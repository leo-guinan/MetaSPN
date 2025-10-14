# Makefile for MetaSPN Rulebook
# Compiles the LaTeX rulebook into PDF format

# Main document
MAIN = main
OUTPUT = MetaSPN_Rulebook_v1.0

# LaTeX compiler
LATEX = pdflatex
BIBTEX = bibtex

# Compiler flags
LATEX_FLAGS = -interaction=nonstopmode -halt-on-error

# Directories
BUILD_DIR = build
OUTPUT_DIR = output

# All chapter files
CHAPTERS = chapters/01_philosophy.tex \
           chapters/02_components.tex \
           chapters/03_classes.tex \
           chapters/04_divisions.tex \
           chapters/05_match_format.tex \
           chapters/06_coaching.tex \
           chapters/07_scoring.tex \
           chapters/08_integrity.tex \
           chapters/09_advancement.tex \
           chapters/10_governance.tex \
           chapters/11_spectator.tex \
           chapters/12_future.tex \
           chapters/appendix_technical.tex \
           chapters/appendix_glossary.tex

.PHONY: all clean build init help view

# Default target
all: init build

# Initialize directories
init:
	@echo "Creating build directories..."
	@mkdir -p $(BUILD_DIR)
	@mkdir -p $(OUTPUT_DIR)

# Build the full rulebook
build: $(MAIN).tex $(CHAPTERS)
	@echo "Compiling LaTeX document (pass 1)..."
	@$(LATEX) $(LATEX_FLAGS) -output-directory=$(BUILD_DIR) $(MAIN).tex
	@echo "Compiling LaTeX document (pass 2 - for references)..."
	@$(LATEX) $(LATEX_FLAGS) -output-directory=$(BUILD_DIR) $(MAIN).tex
	@echo "Compiling LaTeX document (pass 3 - final)..."
	@$(LATEX) $(LATEX_FLAGS) -output-directory=$(BUILD_DIR) $(MAIN).tex
	@echo "Copying final PDF to output directory..."
	@cp $(BUILD_DIR)/$(MAIN).pdf $(OUTPUT_DIR)/$(OUTPUT).pdf
	@echo ""
	@echo "✅ Build complete! PDF saved as: $(OUTPUT_DIR)/$(OUTPUT).pdf"

# Quick build (single pass, for testing)
quick: init
	@echo "Quick compile (single pass)..."
	@$(LATEX) $(LATEX_FLAGS) -output-directory=$(BUILD_DIR) $(MAIN).tex
	@cp $(BUILD_DIR)/$(MAIN).pdf $(OUTPUT_DIR)/$(OUTPUT).pdf
	@echo "Quick build complete: $(OUTPUT_DIR)/$(OUTPUT).pdf"

# Clean build artifacts
clean:
	@echo "Cleaning build artifacts..."
	@rm -rf $(BUILD_DIR)
	@rm -rf $(OUTPUT_DIR)
	@echo "Clean complete."

# View the compiled PDF (macOS)
view: build
	@echo "Opening PDF..."
	@open $(OUTPUT_DIR)/$(OUTPUT).pdf

# Display help
help:
	@echo "MetaSPN Rulebook - Build System"
	@echo ""
	@echo "Available targets:"
	@echo "  make          - Initialize and build the full rulebook (default)"
	@echo "  make build    - Compile the LaTeX document to PDF"
	@echo "  make quick    - Single-pass compile (faster, for testing)"
	@echo "  make clean    - Remove all build artifacts"
	@echo "  make view     - Build and open the PDF (macOS only)"
	@echo "  make help     - Display this help message"
	@echo ""
	@echo "Output location: $(OUTPUT_DIR)/$(OUTPUT).pdf"

