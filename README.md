# csv-duplicate-manage
A Streamlit application for finding and managing duplicates in CSV files, with a special focus on media tracker data. This tool helps you clean your data by providing advanced duplicate detection methods and flexible merge strategies.

## Project Overview

CSV Duplicate Manager is designed to solve the common problem of duplicate entries in tabular data, especially for users who track media consumption (movies, TV shows, books, etc.). It provides a user-friendly interface with smart algorithms to detect various types of duplicates that might otherwise be hard to find.

### Key Features

- **Multiple Duplicate Detection Methods**:
  - ✅ **Exact Match**: Find identical entries across selected columns
  - ✅ **Case-Insensitive**: Detect duplicates regardless of letter case (e.g., "Breaking Bad" = "breaking bad")
  - ✅ **Whitespace-Insensitive**: Ignore extra spaces when comparing entries (e.g., "The Office" = "The  Office")

- **Intelligent Data Handling**:
  - ✅ **Smart Merging**: Combine information from duplicate entries using various strategies
  - ✅ **Value Preservation**: Keep the most complete information when consolidating duplicates
  - ✅ **Customizable Fields**: Select which columns to check for duplicates and which to merge

- **User Experience**:
  - ✅ **Visual Comparison**: Side-by-side visualization of original and cleaned data
  - ✅ **Progress Indicators**: Animated loading states during processing
  - ✅ **Intuitive UI**: Clean, straightforward interface built with Streamlit
  - ✅ **Export Options**: Download your cleaned data in CSV format

## Getting Started

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/csv-duplicate-manager.git
cd csv-duplicate-manager

# Set up requirements (first time only)
python setup.py

# Install dependencies
pip install -r requirements.txt

# Run the application
streamlit run app.py
```

### Quick Demo

For a quick demo with sample data:

```bash
# Just run the demo script
python run_demo.py
```

This will automatically check for dependencies, install them if needed, and start the application with the included demo data.

## Usage Guide

### Basic Workflow

1. **Upload Data**: Start by uploading your CSV file (or use the included demo data)
2. **Select Columns**: Choose which columns to check for duplicates
3. **Choose Detection Method**: Select how you want to identify duplicates:
   - Exact match (default)
   - Case-insensitive
   - Whitespace-insensitive
4. **Find Duplicates**: The application will analyze your data and show potential duplicates
5. **Select Merge Strategy**: Choose how to handle the duplicate entries:
   - Keep first occurrence only
   - Keep last occurrence only
   - Merge all values (preserving non-empty fields)
   - Merge with preference for longest text values
6. **Process Data**: Apply your selected strategy to clean the data
7. **Review & Export**: Check the results and download your cleaned CSV file

### Example Use Cases

- **Media Collections**: Clean up TV show/movie watchlists with inconsistent naming
- **Book Libraries**: Consolidate reading lists with duplicate entries
- **Music Playlists**: Remove duplicate songs with slightly different titles
- **Contact Lists**: Merge duplicate contacts with complementary information
- **Product Catalogs**: Clean e-commerce product lists with duplicate items

## Demo Data

The repository includes a sample dataset (`demo_data.csv`) with examples of different types of duplicates to help you understand how the system works.

## Technical Details

### Requirements

- Python 3.7+
- Streamlit 1.22.0+
- Pandas 1.5.0+
- NumPy 1.23.0+

See `dependencies_for_github.txt` for the complete list of dependencies.

### Project Structure

- `app.py`: Main application file
- `utils/`: Helper modules for data processing
  - `duplicate_handler.py`: Core algorithms for finding and processing duplicates
- `demo_data.csv`: Sample data for testing
- `run_demo.py`: Script to quickly start the demo version
- `.github/workflows/`: CI/CD configuration

## Deployment Options

### Local Development
Run the application locally as described in the Installation section.

### GitHub Pages
This repository includes GitHub Actions workflows for basic checks when you push changes.

### Streamlit Cloud
For public hosting:
1. Push this code to GitHub
2. Visit [Streamlit Cloud](https://streamlit.io/cloud)
3. Connect your GitHub repository
4. Select app.py as the main file
5. Deploy!

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License
