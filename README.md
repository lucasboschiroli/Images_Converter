# UniFiles Converter +*!¡

A simple yet powerful command-line tool to convert images, videos, audio files, documents, and spreadsheets between various formats.

## Features

- **Multi-format image conversion**: JPG, PNG, GIF, BMP, TIFF, WEBP, ICO
- **Video conversion**: MP4, AVI, MKV, MOV, WEBM, GIF
- **Audio conversion**: MP3, WAV, OGG, FLAC, M4A, AAC
- **Document conversion**: PDF, DOCX, TXT
- **Excel conversion**: XLS, XLSX
- **Batch processing**: Convert entire folders at once
- **High-quality output**: Preserves quality during conversion
- **Auto-detection**: Automatically detects file types
- **Simple interface**: Easy-to-use command-line tool

## Prerequisites

- Python 3.7 or higher
- ffmpeg (required for video/audio conversion)
- Pillow (required for image conversion)
- python-docx (required for DOCX conversion)
- PyPDF2 (required for PDF conversion)
- pdf2docx (required for PDF to DOCX conversion)
- reportlab (required for TXT to PDF conversion)
-openpyxl (required for Excel conversion)
- xlrd (required for XLS file reading)

## Installation

1. **Clone or download this repository**

2. **Install required Python packages:**
   
   **For images, videos, and audio:**
   ```bash
   pip install Pillow
   ```
   
   **For document conversion:**
   ```bash
   pip install python-docx PyPDF2 pdf2docx reportlab
   ```
   
   **For Excel conversion:**
   ```bash
   pip install openpyxl xlrd
   ```
   
   **Or install everything at once:**
   ```bash
   pip install Pillow python-docx PyPDF2 pdf2docx reportlab openpyxl xlrd
   ```

3. **Install ffmpeg (required for video/audio):**
   
   **Windows:**
   ```bash
   winget install ffmpeg
   ```
   
   **macOS:**
   ```bash
   brew install ffmpeg
   ```
   
   **Linux:**
   ```bash
   sudo apt install ffmpeg
   ```

## Usage

### Convert a single file

```bash
python converter.py <input_file> <output_format>
```

### Batch convert multiple files

```bash
python converter.py --batch <directory> <output_format>
```

## Examples

```bash
# Convert image formats
python converter.py photo.png jpg
python converter.py image.jpg webp

# Convert video formats
python converter.py video.mp4 webm
python converter.py movie.avi mkv
python converter.py clip.mp4 gif

# Convert audio formats
python converter.py song.wav mp3
python converter.py audio.flac ogg

# Convert documents
python converter.py document.docx pdf
python converter.py file.pdf txt
python converter.py notes.txt docx

# Convert Excel files
python converter.py spreadsheet.xls xlsx

# Batch convert all files in a folder
python converter.py --batch ./my_images png
python converter.py --batch ./videos mp4
python converter.py --batch ./documents pdf
```

## Output

Converted files are saved in the same directory as the original file with the new file extension.

## Troubleshooting

### "pip is not recognized"
Use `python -m pip install <package>` instead

### "ffmpeg is not installed"
Install ffmpeg using the instructions above. Required for video and audio conversions.

### "Module not found" errors
Install the missing package:
- Images: `pip install Pillow`
- Documents: `pip install python-docx PyPDF2 pdf2docx reportlab`
- Excel: `pip install openpyxl xlrd`

### Conversion fails
- Check that the input file exists and is not corrupted
- Verify the output format is supported for that file type
- Some document conversions may require additional system dependencies

### Python 3.14 compatibility issues
If you encounter build errors with newer Python versions, try:
```bash
pip install --only-binary :all: <package_name>
```

## Supported Conversions

### Images
JPG ↔ PNG ↔ GIF ↔ BMP ↔ TIFF ↔ WEBP ↔ ICO

### Videos
MP4 ↔ AVI ↔ MKV ↔ MOV ↔ WEBM ↔ GIF

### Audio
MP3 ↔ WAV ↔ OGG ↔ FLAC ↔ M4A ↔ AAC

### Documents
- PDF → DOCX, TXT
- DOCX → PDF, TXT
- TXT → PDF, DOCX

### Excel
XLS → XLSX

## Legal Notice

This tool is for personal use. Please respect copyright laws and only convert files you have the right to modify.

## License

This project is open source and available under the MIT License.

## Credits

Built with:
- [Pillow](https://python-pillow.org/) - Image processing
- [FFmpeg](https://ffmpeg.org/) - Video and audio conversion
- [python-docx](https://python-docx.readthedocs.io/) - Word document processing
- [PyPDF2](https://pypdf2.readthedocs.io/) - PDF processing
- [ReportLab](https://www.reportlab.com/) - PDF generation
- [openpyxl](https://openpyxl.readthedocs.io/) - Excel file processing
