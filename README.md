# Sort Downloads

A simple bash script to automatically organize your Downloads folder by categorizing files into folders based on their file extensions.

## Features

- **Automatic sorting** - Files are automatically moved to category folders
- **Case insensitive** - Matches file extensions regardless of case (`.JPG` = `.jpg`)
- **Directory handling** - Unknown folders are moved to `Dirs/`
- **Easy customization** - Add or modify file categories in the config

## Categories

| Folder | Extensions |
|--------|------------|
| Pictures | jpg, jpeg, png, gif, webp, svg, heic, bmp, tiff |
| Videos | mp4, mkv, webm, mov, avi, flv, m4v |
| Archives | zip, tar.gz, tar, rar, 7z, gz, bz2, iso |
| Documents | pdf, doc, docx, xls, xlsx, ppt, pptx, txt, md, odt, rtf, csv |
| Music | mp3, flac, wav, aac, ogg, m4r, m4a |
| Books | epub, mobi, azw3, djvu, cbz, cbr |
| Programs | exe, AppImage, deb, rpm, sh, py, js, jar, pl, go |
| Fonts | ttf, otf, woff, woff2 |

## Installation

```bash
# Clone or download this repository
git clone https://github.com/yourusername/sort-downloads.git
cd sort-downloads

# Make executable
chmod +x sort-downloads

# Run the script
./sort-downloads
```

## Usage

Simply run the script:

```bash
./sort-downloads
```

Your Downloads folder will be organized into the following structure:

```
~/Downloads/
├── Pictures/
├── Videos/
├── Archives/
├── Documents/
├── Music/
├── Books/
├── Programs/
├── Fonts/
├── Dirs/
└── Others/
```

## Configuration

Edit the `FILE_CATEGORIES` associative array in the script to customize categories and extensions:

```bash
declare -A FILE_CATEGORIES=(
  [Pictures]="jpg jpeg png gif webp"
  [Videos]="mp4 mkv webm mov"
  # Add more categories here
)
```

## License

MIT
