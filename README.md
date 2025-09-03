# Enhanced LaTeX Comment System with FontAwesome Icons

[![LaTeX Build Status](https://github.com/sergiorico/latex_comments_system/workflows/LaTeX%20Build%20Status/badge.svg)](https://github.com/sergiorico/latex_comments_system/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![LaTeX](https://img.shields.io/badge/LaTeX-008080?logo=latex&logoColor=white)](https://www.latex-project.org/)
[![FontAwesome](https://img.shields.io/badge/FontAwesome-339AF0?logo=fontawesome&logoColor=white)](https://fontawesome.com/)
[![GitHub release](https://img.shields.io/github/release/sergiorico/latex_comments_system.svg)](https://github.com/sergiorico/latex_comments_system/releases)
[![GitHub stars](https://img.shields.io/github/stars/sergiorico/latex_comments_system.svg)](https://github.com/sergiorico/latex_comments_system/stargazers)

This repository provides an enhanced LaTeX comment system with FontAwesome icons for collaborative writing, demonstrated across three major academic templates.nhanced LaTeX Comment System with FontAwesome Icons


## Features

- **8 Comment Types**: Each with distinctive FontAwesome icons and colors
- **Multi-Author Support**: Configurable author aliases with color-coded comments
- **Easy Integration**: Simply include `comments.tex` in any LaTeX document

## Comment Types

| Icon | Type | Color | Description |
|------|------|-------|-------------|
| 📝 | `cite` | Blue | Citations needed |
| ✏️ | `edit` | Red | Editorial suggestions |
| 🌐 | `lang` | Orange | Language improvements |
| ⚠️ | `warn` | Purple | Important warnings |
| ✅ | `check` | Green | Verification needed |
| 📊 | `fig` | Cyan | Figure-related comments |
| 📋 | `todo` | Gray | TODO items |
| 👁️ | `review` | Brown | Review suggestions |

## Templates & Examples

The repository includes **pre-compiled PDF examples** that you can view immediately:

### 1. ACM Manuscript ([`sample.tex`](sample.tex) → [`sample.pdf`](sample.pdf))
- **Format**: ACM article format
- **Pages**: 3 pages
- **Features**: Full demonstration with icon table and examples
- **📄 [View PDF](sample.pdf)**

### 2. IEEE Magazine ([`sample-ieee-magazine.tex`](sample-ieee-magazine.tex) → [`sample-ieee-magazine.pdf`](sample-ieee-magazine.pdf))  
- **Format**: IEEE magazine style
- **Pages**: 2 pages
- **Features**: Two-column layout with condensed examples
- **📄 [View PDF](sample-ieee-magazine.pdf)**

### 3. Elsevier Single-Column ([`sample-elsevier.tex`](sample-elsevier.tex) → [`sample-elsevier.pdf`](sample-elsevier.pdf))
- **Format**: Elsevier article format
- **Pages**: 5 pages (single-column)
- **Features**: Extended examples in single-column layout
- **📄 [View PDF](sample-elsevier.pdf)**

**Compilation**: If you want to recompile, use `pdflatex <filename>.tex`

## Quick Start

1. **Basic Usage**:
   ```latex
   \input{comments.tex}
   \addnote[todo]{This needs to be completed}
   \addnote[cite]{Add reference here}
   ```

2. **Natural Author Commands**:
   ```latex
   % Set up author names and create natural commands
   \renewcommand{\AuthorOneName}{John Snow}
   \renewcommand{\AuthorTwoName}{Pepito Perez}
   \createauthorcommand{john}{1}
   \createauthorcommand{pepito}{2}
   
   % Use natural commands
   \john{This is John's comment}
   \pepito{This is Pepito's comment}
   ```

3. **Visibility Control**:
   ```latex
   \showcomments    % Show all comments (default)
   \hidecomments    % Hide all comments for camera-ready
   ```

   ```

## Enhanced Features

### Natural Author Commands

You can now use natural names based on the author's first name:

- `\john{comment}` for John Snow's comments
- `\pepito{comment}` for Pepito Perez's comments  
- `\maria{comment}` for Maria Garcia's comments
- `\alex{comment}` for Alex Chen's comments

### Convenient Comment Type Commands
Use specific comment types with the simple syntax:

- `\addnote[cite]{comment}` - Citation needed
- `\addnote[edit]{comment}` - Editorial suggestion
- `\addnote[todo]{comment}` - TODO item
- `\addnote[warn]{comment}` - Warning
- `\addnote[check]{comment}` - Check needed
- `\addnote[fig]{comment}` - Figure comment
- `\addnote[lang]{comment}` - Language improvement
- `\addnote[review]{comment}` - Review needed

### Visibility Control
Easily toggle all comments on/off:

- `\showcomments` - Make all comments visible (default)
- `\hidecomments` - Hide all comments for camera-ready version

## Dependencies

The system requires these LaTeX packages:
- `fontawesome5` - For icons
- `xcolor` - For colors  
- `xspace` - For spacing
- `etoolbox` - For string comparisons
- `booktabs` - For tables (Elsevier template)
- `graphicx` - For graphics (IEEE template)

## Files

### Core System
- `comments.tex` - Core comment system implementation
- `references.bib` - Clean bibliography for all templates

### LaTeX Templates & Examples
- `sample.tex` + `sample.pdf` - ACM manuscript demonstration
- `sample-ieee-magazine.tex` + `sample-ieee-magazine.pdf` - IEEE magazine demonstration  
- `sample-elsevier.tex` + `sample-elsevier.pdf` - Elsevier single-column demonstration

**📄 All PDFs are pre-compiled and ready to view!**

## Template Status

✅ **ACM Manuscript** ([sample.pdf](sample.pdf)): 3 pages, fully functional with all icons  
✅ **IEEE Magazine** ([sample-ieee-magazine.pdf](sample-ieee-magazine.pdf)): 2 pages, compact layout with all features  
✅ **Elsevier Single-Column** ([sample-elsevier.pdf](sample-elsevier.pdf)): 5 pages, extended examples working

**All templates include pre-compiled PDFs** - view them directly in your browser! No compilation needed to see the results.

## Getting Started

**📄 View Examples Immediately**: All templates include pre-compiled PDFs - just click the links above!

**🚀 Use in Your Project**:
1. Download `comments.tex` 
2. Include it in your LaTeX document: `\input{comments.tex}`
3. Start using `\addnote[type]{comment}` or natural author commands

**🔄 Recompile if Needed**: Use `pdflatex filename.tex` to regenerate PDFs

## Acknowledgments

Made with ❤️ from the heart of Sweden 🇸🇪  
**Mid Sweden University** | *Mittuniversitetet*

*Fostering collaborative academic writing and open-source LaTeX tools.*

## License

This project demonstrates academic LaTeX collaboration tools. Use freely for academic purposes.
