# Flask Portfolio Application

This Flask-based web application serves as a personal portfolio, showcasing a timeline of events, a reading list, projects, and professional experiences. It utilizes static JSON files for data management and provides a variety of routes to display content dynamically.

## Features

- **Homepage:** Displays a welcoming message with a consistent theme across the site.
- **Timeline:** Presents a chronological list of events sourced from a JSON file.
- **Reading List:** Shows a curated list of books or articles with details fetched from a JSON file.
- **Projects:** Lists projects with the ability to sort and filter based on tags and weights. Projects are displayed in descending order of their weights.
- **Experiences:** Displays professional experiences with sorting based on weights.
- **Project/Experience Details:** Provides detailed information about a specific project or experience, including content from an associated HTML file if not included in the JSON.
- **Error Handling:** Custom 404 error page for handling not-found errors.

## Installation and Setup

### Prerequisites

- **Python:** Ensure Python 3.6 or higher is installed.
- **Flask:** This application requires Flask to run. Install it via pip.

### Steps to Install

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/Portfolio-Flask.git
   ```
   
2. **Navigate to the Project Directory:**
   ```bash
   cd Portfolio-Flask
   ```

3. **Install Dependencies:**
   Create a virtual environment (recommended) and install Flask.
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install flask
   ```

4. **Run the Application:**
   ```bash
   python app.py
   ```

5. **Access the Application:**
   Open a web browser and go to `http://127.0.0.1:5000`.

## File Structure

- **app.py:** Main application file containing routes and business logic.
- **templates/:** Directory containing HTML templates.
  - **home.html:** Template for the homepage.
  - **timeline.html:** Template for the timeline page.
  - **reading.html:** Template for the reading list page.
  - **projects.html:** Template for displaying projects.
  - **project.html:** Template for detailed view of a project or experience.
  - **404.html:** Custom template for 404 error pages.
- **static/:** Directory for static assets.
  - **files/timeline.json:** JSON file containing timeline data.
  - **files/reading.json:** JSON file containing reading list data.
  - **projects/projects.json:** JSON file containing project data with `link`, `description`, and `weight`.
  - **experiences/experiences.json:** JSON file containing experience data with `link`, `description`, and `weight`.
- **static/<path>/**/*.html:** Optional HTML files for detailed project or experience descriptions.

## Routes

- `/`: Displays the homepage.
- `/timeline`: Displays the timeline of events.
- `/reading`: Displays the reading list.
- `/projects`: Lists projects with optional tag filtering and sorting.
- `/projects/<title>`: Shows detailed information for a specific project or experience.
- `/experiences`: Lists professional experiences.
- `/404`: Custom 404 error page for handling not-found errors.

## Data Structure

### JSON Files

- **timeline.json:** Array of timeline events. Each event should have properties such as `date`, `title`, and `description`.
- **reading.json:** Array of reading list items. Each item should have properties like `title`, `author`, and `summary`.
- **projects.json:** JSON object with a `projects` key containing an array of projects. Each project includes:
  - `link`: Identifier used in URLs.
  - `description`: Detailed description of the project.
  - `weight`: Numeric value used to sort projects.
- **experiences.json:** JSON object with an `experiences` key containing an array of experiences. Each experience includes:
  - `link`: Identifier used in URLs.
  - `description`: Detailed description of the experience.
  - `weight`: Numeric value used to sort experiences.

## Application Functions

- **`get_static_file(path)`**: Returns the absolute path for a static file based on the provided path.
- **`get_static_json(path)`**: Loads and returns the content of a JSON file located at the provided path.

## Error Handling

- **404 Error Page:** Custom page displayed when a requested resource is not found.

## Contributions

Contributions are welcome! To contribute to this project, please fork the repository, make your changes, and submit a pull request.

## Contact

For questions or further information, please contact:

- **Name:** Bevina R
- **Email:** bevina2110@gmail.com
- **GitHub:** [yourusername](https://github.com/Bevinaa)

