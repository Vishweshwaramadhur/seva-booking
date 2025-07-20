
# Temple Seva Management System

A web application built with Flask for managing temple sevas (religious services). This system allows temple administrators to manage seva offerings and generate bills for devotees.

## Features

### Seva Management
- Add new sevas with name, price, and description
- Edit existing seva details
- Delete sevas from the system
- View all sevas in an organized list

### Billing System
- Select multiple sevas using checkboxes
- Generate itemized bills with total amount
- Professional bill format with date and time stamp

## Technologies Used

- **Backend**: Python 3.7+, Flask 2.3.2
- **Database**: SQLite
- **Frontend**: HTML5, CSS3, JavaScript
- **Styling**: Custom CSS with responsive design

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/temple-seva-management.git
cd temple-seva-management
```

2. Create a virtual environment
```bash
python -m venv venv
```

3. Activate the virtual environment
```bash
# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

4. Install required packages
```bash
pip install -r requirements.txt
```

5. Run the application
```bash
python app.py
```

6. Open your web browser and navigate to
```
http://localhost:5000
```

## Project Structure

```
temple-seva-management/
│
├── app.py              # Main Flask application
├── requirements.txt    # Python dependencies
├── README.md          # Project documentation
│
├── static/            # Static files
│   ├── style.css     # CSS styles
│   └── script.js     # JavaScript functionality
│
├── templates/         # HTML templates
│   └── index.html    # Main page
│
└── sevas.db          # SQLite database (auto-created)
```

## Usage

### Adding a New Seva
1. Fill in the seva name in the "Seva Name" field
2. Enter the amount in rupees
3. Optionally add a description
4. Click "Add Seva" button

### Editing a Seva
1. Click the "Edit" button next to the seva
2. Modify the details in the popup form
3. Click "Save Changes"

### Deleting a Seva
1. Click the "Delete" button next to the seva
2. Confirm the deletion when prompted

### Generating Bills
1. Select sevas using the checkboxes
2. Click "Calculate Bill for Selected Sevas"
3. View the generated bill with total amount

## Database Schema

```sql
CREATE TABLE sevas (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    rupees INTEGER NOT NULL,
    description TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Default Sevas

The application comes pre-loaded with 22 common temple sevas including:
- Shashwatha Pooja
- Mahapooja
- Alankara Pooje
- Ganapathi Homam
- And more...

## API Endpoints

| Method | Endpoint            | Description                       |
| ------ | ------------------- | --------------------------------- |
| GET    | `/`                 | Display main page with all sevas  |
| POST   | `/add_seva`         | Add a new seva                    |
| POST   | `/edit_seva/<id>`   | Edit existing seva                |
| POST   | `/delete_seva/<id>` | Delete a seva                     |
| POST   | `/calculate_bill`   | Calculate bill for selected sevas |

## Future Enhancements

- User authentication for temple staff
- Devotee information management
- Payment tracking
- Receipt printing functionality
- Export bills to PDF
- Monthly/yearly revenue reports
- Multi-language support
- SMS/Email notifications

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.

