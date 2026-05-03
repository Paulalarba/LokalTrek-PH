# 🌴 LokalTrek PH: The Authentic Philippine Travel Hub

**LokalTrek PH** is a nationwide travel and booking directory built on ASP.NET Core 10. It is designed specifically for "flashpackers"—travelers who want raw, authentic local experiences (eating street food, meeting local guides) but are willing to pay for convenience, comfort, and a seamless booking process.

Instead of generic hotel listings, LokalTrek PH focuses on **Curated Experiences**, **Local Vendors**, and **Gastro-Tourism** across the 7,600+ islands of the Philippines, bridging the gap between local island economies and digital-first travelers.

---

## ✨ Key Features

### 🤖 AI-Powered Capabilities
*   **Visual Itinerary Generation:** Users can upload a photo or a link to a social media reel (e.g., a hidden waterfall in Sagada or a surfing spot in Siargao). The platform's AI vision tools identify the location, pull relevant local vendors from the database, and generate a cohesive, bookable 3-day itinerary.
*   **Conversational Travel Assistant (LokalBot):** An integrated AI chatbot that understands natural language queries like, *"Find me a romantic weekend in Bantayan under ₱3,000/night near MJ Square,"* and cross-references user intent with our database to provide instant, personalized booking links.
*   **Predictive Travel Timing:** Machine learning algorithms that analyze historical weather patterns (Amihan vs. Habagat seasons) and ferry cancellation rates to recommend the safest and most optimal days to book island transfers.

### 🎒 Core Platform Features
*   **Hierarchical Destination Browsing:** A structured database that prevents geographical mismatches, allowing users to drill down precisely from Region ➔ Province ➔ Island/Municipality.
*   **"Catch and Cook" & Curated Packages:** A direct booking engine for specialized local experiences (e.g., booking a local fisherman's boat alongside a local chef to cook the catch).
*   **Vendor Subscription Portal:** A secure dashboard for local tricycle drivers, homestays, and eateries to manage their "Featured Partner" subscriptions, update their menus, and adjust pricing.
*   **Smart Filtering:** Filter trips by hyper-specific needs such as "Kid-Friendly," "Internet Speed" (for digital nomads), or "Dietary Restrictions."

---

## 🛠️ Tech Stack

*   **Framework:** ASP.NET Core 10 (MVC Architecture)
*   **Database:** Microsoft SQL Server (or SQLite for local development)
*   **ORM:** Entity Framework Core 10
*   **AI Integration:** Semantic Kernel (for connecting .NET directly to LLMs/AI APIs)
*   **Frontend:** Razor Views, Bootstrap 5, and vanilla JavaScript
*   **Authentication:** ASP.NET Core Identity for secure user and vendor logins

---

## 🗄️ Database Architecture

The data structure is built to scale across the entire Philippines using hierarchical geography:

1.  **`Destination` Model:** The root model mapping Provinces (e.g., "Cebu") to specific Islands or Cities (e.g., "Bantayan").
2.  **`LocalVendor` Model:** Tied to a Destination. Stores data for local guides, restaurants, and transport rentals.
3.  **`CuratedPackage` Model:** Pre-bundled itineraries combining multiple vendors (e.g., "3-Day Surf & Eat").
4.  **`Booking` Model:** Tracks user transactions, dates, and selected packages.

*(Note: For development and testing purposes, the database is seeded with mock data for three flagship destinations: Bantayan Island, Siargao, and Sagada).*

---

## 🚀 Getting Started

Follow these steps to run the LokalTrek PH project locally on your machine.

### Prerequisites
*   [Visual Studio 2022](https://visualstudio.microsoft.com/) (or newer) / Visual Studio Code
*   [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)
*   SQL Server Express (or LocalDB)

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone [https://github.com/yourusername/LokalTrekPH.git](https://github.com/yourusername/LokalTrekPH.git)
   cd LokalTrekPH
