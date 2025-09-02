# Enhanced LaTeX Comment System with FontAwesome Icons

[![LaTeX Build Status](https://github.com/USER/REPO/workflows/LaTeX%20Build%20Status/badge.svg)](https://github.com/sergiorico/latex_comments_system/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![LaTeX](https://img.shields.io/badge/LaTeX-008080?logo=latex&logoColor=white)](https://www.latex-project.org/)
[![FontAwesome](https://img.shields.io/badge/FontAwesome-339AF0?logo=fontawesome&logoColor=white)](https://fontawesome.com/)
[![GitHub release](https://img.shields.io/github/release/USER/REPO.svg)](https://github.com/USER/REPO/releases)
[![GitHub stars](https://img.shields.io/github/stars/USER/REPO.svg)](https://github.com/USER/REPO/stargazers)

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

## Templates

### 1. ACM Manuscript (`sample.tex`)
- **Format**: ACM article format
- **Pages**: 3 pages
- **Compilation**: `pdflatex sample.tex`
- **Features**: Full demonstration with icon table and examples

### 2. IEEE Magazine (`sample-ieee-magazine.tex`)  
- **Format**: IEEE magazine style
- **Pages**: 2 pages
- **Compilation**: `pdflatex sample-ieee-magazine.tex`
- **Features**: Two-column layout with condensed examples

### 3. Elsevier Single-Column (`sample-elsevier.tex`)
- **Format**: Elsevier article format
- **Pages**: 5 pages (single-column)
- **Compilation**: `pdflatex sample-elsevier.tex`
- **Features**: Extended examples in single-column layout

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

- `comments.tex` - Core comment system implementation
- `sample.tex` - ACM manuscript demonstration
- `sample-ieee-magazine.tex` - IEEE magazine demonstration  
- `sample-elsevier.tex` - Elsevier single-column demonstration
- `references.bib` - Clean bibliography for all templates

## Template Status

✅ **ACM Manuscript**: 3 pages, fully functional with all icons  
✅ **IEEE Magazine**: 2 pages, compact layout with all features  
✅ **Elsevier Single-Column**: 5 pages, extended examples working

All templates compile successfully with FontAwesome icons displaying properly.

## Continuous Integration

This repository includes GitHub Actions that automatically:

- **Build Check**: Compiles all templates on every push/PR to ensure they work
- **Release PDFs**: Creates releases with compiled PDFs when you tag a version

### Usage:
1. **Automatic builds**: Push changes and GitHub will compile all templates
2. **Create releases**: Tag a version with `git tag v1.0 && git push --tags` to generate a release with PDFs

### Artifacts:
- Build artifacts are available for 30 days after each successful build
- Release PDFs are permanently available on the releases page

## Acknowledgments

Made with ❤️ from the heart of Sweden 🇸🇪  
**Mid Sweden University** | *Mittuniversitetet*

*Fostering collaborative academic writing and open-source LaTeX tools.*

## License

This project demonstrates academic LaTeX collaboration tools. Use freely for academic purposes.
