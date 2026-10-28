Orbixa — Travel Together, Explore More

**Orbixa** is a travel companion web application designed to help travelers discover destinations, connect with like-minded people, plan trips together, and manage shared travel expenses.

The platform makes exploring new places more social, organized, and enjoyable.

Features:

- **User Authentication** — Register and log in securely using password hashing.
- **Language Selection** — Choose a preferred language during onboarding.
- **Destination Explorer** — Browse destinations and discover places to visit.
- **Place Categories** — Explore tourist attractions, restaurants, hotels, and activities.
- **Automatic Place Photos** — Search for relevant place images using Wikimedia Commons.
- **Trip Creation** — Create trips with travel dates, group size, budget, and activity details.
- **Recommended Trips** — Discover trips based on saved travel preferences and interests.
- **Trip Joining** — Request to join trips created by other travelers.
- **Group Communication** — Exchange messages with approved trip members.
- **Expense Management** — Record and track shared trip expenses.
- **User Profiles** — Manage personal details, travel interests, and preferences.
- **Admin Management** — Manage destinations and place listings.

Tech Stack

- **Backend:** Python, Flask
- **Database:** SQLite, Flask-SQLAlchemy
- **Frontend:** HTML, CSS, JavaScript, Jinja2
- **Authentication:** Werkzeug password hashing
- **Real-Time Communication:** Flask-SocketIO
- **Form Security:** Flask-WTF CSRF protection
- **Image Source:** Wikimedia Commons API
- **Version Control:** Git and GitHub

Project Structure

```text
Orbixa_Travel_Companion/
├── app.py
├── add_place_photos.py
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── auth.html
│   ├── dashboard.html
│   ├── destinations.html
│   ├── destination_detail.html
│   ├── create_trip.html
│   ├── trip_detail.html
│   ├── profile.html
│   └── admin.html
├── static/
│   ├── css/
│   └── js/
├── .gitignore
└── README.md
```

*The structure above represents the main application files; additional files may be present in the project.*

Installation and Setup

Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Orbixa_Travel_Companion.git
cd Orbixa_Travel_Companion
```

Replace `YOUR-USERNAME` with your GitHub username.

Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies

Install the packages used by the application:

```bash
python -m pip install Flask Flask-SQLAlchemy Flask-SocketIO Flask-WTF requests
```

Configure the application

Set a secret key before running the application.

In PowerShell:

```powershell
$env:ORBIXA_SECRET_KEY = "replace-with-a-long-random-secret"
```

For local development, the application uses SQLite by default. The database and starter destination data are initialized by the application.

Run Orbixa

```bash
python app.py
```

Open the local application in your browser at:

http://127.0.0.1:5000

Add automatic place photos

After installing the dependencies and ensuring the application is configured correctly, run:

```bash
python add_place_photos.py
```

The script searches Wikimedia Commons for place images and saves found image URLs to the existing database. Existing place photos are preserved.

Security Notes

- Passwords are stored using password hashing.
- Keep secret keys, credentials, and environment files out of GitHub.
- Do not commit databases containing personal or account information.
- Configure a strong secret key before deployment.
- Set secure cookie options and use HTTPS in production.
- Configure and verify administrator credentials using environment variables.

Future Enhancements

- More destination-specific photos and information.
- Improved travel recommendations.
- Enhanced trip planning and itinerary management.
- Additional language support.
- Expanded safety and traveler verification features.
- Deployment to a production hosting platform.

Project Goal

Orbixa aims to make travel more connected by bringing people with similar interests and destinations together, helping them discover places, organize group trips, communicate, and manage expenses.
