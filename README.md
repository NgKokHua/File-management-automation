# File Management Automation 🗂️

An intelligent Python script that automatically organizes your Downloads folder by sorting files into categorized directories based on their file types. Never manually organize your downloads again!

## ✨ Features

- **🔍 Real-time File Monitoring** - Continuously watches your Downloads folder for new files
- **📁 Automatic Organization** - Sorts files by type into dedicated folders
- **🔄 Existing File Processing** - Processes files already in Downloads when script starts
- **⚡ Smart File Handling** - Handles duplicate filenames automatically
- **🛡️ Error Resilience** - Gracefully handles permission errors and files in use
- **📝 Detailed Logging** - Tracks all file movements with timestamps
- **🎯 Multiple File Types** - Supports images, videos, documents, and audio files

## 📂 File Organization

Your files are automatically sorted into these directories:

| File Type | Destination Folder | Supported Extensions |
|-----------|-------------------|---------------------|
| **Images** | `Desktop/Downloaded image` | `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`, `.tiff`, `.bmp`, `.svg`, `.ico`, and more |
| **Videos** | `Desktop/Downloaded video` | `.mp4`, `.avi`, `.mov`, `.wmv`, `.flv`, `.webm`, `.mkv`, and more |
| **Documents** | `Desktop/Downloaded document` | `.pdf`, `.doc`, `.docx`, `.xls`, `.xlsx`, `.ppt`, `.pptx`, `.txt`, and more |
| **Audio (Small)** | `Downloads/Sound` | Files < 10MB or containing "SFX" |
| **Audio (Large)** | `Desktop/Sound/Music` | Audio files > 10MB |

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- Windows OS (paths are Windows-specific)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/NgKokHua/File-management-automation.git
   cd File-management-automation
   ```

2. **Set up virtual environment**
   ```bash
   python -m venv myenv
   myenv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install watchdog
   ```

### Usage

1. **Start the file automation**
   ```bash
   myenv\Scripts\python.exe fileAutomation.py
   ```

2. **Watch the magic happen!**
   - The script will first process any existing files in your Downloads folder
   - Then it will continuously monitor for new downloads
   - Files are automatically sorted in real-time

3. **Stop the script**
   - Press `Ctrl+C` in the terminal to stop monitoring

## 📋 Example Output

```
Starting file automation...
Watching directory: C:\Users\YourName\Downloads
Directory exists: True
Processing existing files...
2025-10-30 20:46:32 - Moved image file: vacation_photo.jpg
2025-10-30 20:46:32 - Moved document file: resume.pdf
2025-10-30 20:46:33 - Moved video file: tutorial.mp4
Existing files processed.
File monitoring started. Press Ctrl+C to stop.
```

## 🔧 Configuration

You can customize the script by editing the directory paths in `fileAutomation.py`:

```python
# Source directory (where files are downloaded)
source_dir = r"C:\Users\YourName\Downloads"

# Destination directories
dest_dir_image = r"C:\Users\YourName\Desktop\Downloaded image"
dest_dir_video = r"C:\Users\YourName\Desktop\Downloaded video"
dest_dir_documents = r"C:\Users\YourName\Desktop\Downloaded document"
# ... and more
```

## 🛠️ Technical Details

- **File Monitoring**: Uses the `watchdog` library for efficient file system monitoring
- **Path Handling**: Properly handles Windows paths with `os.path.join()`
- **Error Handling**: Comprehensive error handling for permission issues
- **Logging**: Built-in logging with timestamps for debugging and monitoring
- **Performance**: Lightweight and efficient, minimal system resource usage

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🐛 Troubleshooting

**Script stops running:**
- Check if files are being used by other programs
- Ensure you have write permissions to destination folders
- Run the script as administrator if needed

**Files not moving:**
- Verify destination folders exist
- Check file extensions are in the supported list
- Look at console output for error messages

**Permission errors:**
- Close files that might be open in other applications
- Run command prompt as administrator
- Check antivirus software isn't blocking file operations

## 👨‍💻 Author

**Ng Kok Hua** - [GitHub Profile](https://github.com/NgKokHua)

---

⭐ **Star this repo if it helped you organize your files!** ⭐
