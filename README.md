# 🍽️ Flavor Finder

Welcome to **Flavor Finder**, the ultimate restaurant discovery tool that helps you find your next favorite spot to eat! With the power of Google Places API and a sleek interface, Flavor Finder makes it easy to search for restaurants by city/state or zip code and swipe through recommendations. 🚀

---

## 🌟 Features

- **Restaurant Search**: Search for restaurants near you by zip code or city and state.
- **Detailed Results**: View restaurant names, ratings, addresses, cuisines, phone numbers, and websites.
- **Swipable Card Stack**: Swipe through restaurant recommendations with an intuitive interface.
- **Surprise Me**: Can't decide? Let Flavor Finder pick a restaurant for you!
- **Responsive Design**: Works seamlessly across desktop and mobile devices.
- **Messaging Panel**: Manage chat-like messaging for teams or future use cases.

---

## 🛠️ Setup Instructions

### Prerequisites

1. Install [Java 17+](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html).
2. Install [Node.js](https://nodejs.org/en/) for the frontend.
3. Install [PostgreSQL](https://www.postgresql.org/download/).
4. Set up a Google Cloud project with **Places API** and **Places Photo API** enabled.

---

### Backend Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/flavor-finder.git
   cd flavor-finder/backend
   ```

2. Create a PostgreSQL database:
   ```sql
   CREATE DATABASE flavor_finder;
   ```

3. Configure your database and Google API in `application.properties`:
   ```properties
   # Database Configuration
   spring.datasource.url=jdbc:postgresql://localhost:5432/flavor_finder
   spring.datasource.username=your_db_username
   spring.datasource.password=your_db_password

   # Google Places API
   google.places.baseurl=https://maps.googleapis.com/maps/api/place/textsearch/json
   google.places.key=YOUR_GOOGLE_API_KEY
   ```

4. Build and run the backend server:
   ```bash
   ./mvnw clean install
   ./mvnw spring-boot:run
   ```

   The backend will run at `http://localhost:9000`.

---

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

   The frontend will run at `http://localhost:5173`.

---

## 🎮 How to Use

### Searching for Restaurants

1. Select your preferred search type:
   - **Zip Code**: Enter a zip code to search for nearby restaurants.
   - **City/State**: Enter a city and state for broader results.
2. Click **Search** to fetch restaurants.
3. Swipe through the card stack to explore the results or use **Surprise Me!** for a random suggestion.

---

### Favorite/Skip Restaurants

- Swipe **right** on a card to **favorite** a restaurant.
- Swipe **left** on a card to **skip** a restaurant.
- Favorites and skipped restaurants are saved to your account.

---

## 🌐 API Endpoints

### Backend

| Endpoint                          | Method | Description                                     |
|-----------------------------------|--------|-------------------------------------------------|
| `/api/restaurants/fetch`          | `GET`  | Fetch restaurants based on zip code or city.   |
| `/api/restaurants/favorites`      | `POST` | Add a restaurant to the user's favorites.      |
| `/api/restaurants/skipped`        | `POST` | Skip a restaurant for the user.                |

---

## 💡 Future Enhancements

- **Geolocation**: Automatically detect user location for searches.
- **Review System**: Allow users to leave and view reviews.
- **Group Voting**: Plan outings with group voting on restaurant choices.
- **Dark Mode**: Add a dark mode for enhanced UI experience.

---

## 🧑‍💻 Contributors

- **Danny Ambrose** - Full-Stack Developer

---

## 📧 Support

For issues or feature requests, email us at **support@flavorfinder.com**.

---

## 📝 License

This project is licensed under the **MIT License**.

---

Thank you for using Flavor Finder! Bon Appétit! 🍴
