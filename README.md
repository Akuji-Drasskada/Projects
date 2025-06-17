📘 EventEaseVenueBookingSystem

EventEase is a lightweight, in-memory web application for managing venue bookings, events, and users. Built using ASP.NET Core MVC, it provides a clean UI and basic authentication without using any external database.



 🚀 Features

 ✅ Clean sidebar layout with Bootstrap styling
 ✅ Admin and user login using in-memory authentication
 ✅ Create, list, and delete:

   Venues
   Events
   Bookings

 ✅ Role-based access (Admin-only create/delete)
 ✅ No database required — everything runs in memory!



 🧪 Demo Admin Login

Navigate to:

```
/Auth/Login
```

Use the following credentials:

 Username: `admin`
 Password: `admin123`

After logging in:

 You’ll see `Hello, admin!` and a `Logout` button in the top-right.
 Admins can create/delete events, venues, and bookings.
 Regular users will only see the `Login` option and can view content.



 🛠️ How It Works

 All data (users, venues, events, bookings) is stored in static in-memory lists.
 Role-based access is controlled using `[Authorize(Roles = "Admin")]`.
 Layout consists of a responsive top bar and a vertical sidebar menu.
 Uses Razor Views and ViewModels with validation for form submissions.



 📂 Project Structure (Highlights)

```
├── Controllers/
│   ├── AuthController.cs
│   ├── BookingController.cs
│   ├── EventController.cs
│   ├── VenueController.cs
│
├── Views/
│   ├── Shared/_Layout.cshtml
│   ├── Booking/, Event/, Venue/, Home/
│
├── Data/
│   ├── InMemoryDataStore.cs
│   ├── InMemoryUserStore.cs
│
├── ViewModels/
│   ├── BookingViewModel.cs
│   ├── EventViewModel.cs
│   ├── VenueViewModel.cs
│
├── wwwroot/css/
│   ├── site.css
```



 📦 Requirements

 [.NET SDK 7.0+](https://dotnet.microsoft.com/en-us/download)
 Modern browser (Chrome, Edge, Firefox)



 ▶️ Getting Started

1. Clone or download the repo
2. Open the solution in Visual Studio or run via terminal:

```bash
dotnet run
```

3. Navigate to:

```
https://localhost:{PORT}/Auth/Login
```



 ⚙️ Customisation

You can edit these files to modify behaviour:

 `InMemoryUserStore.cs` — add more users or roles
 `InMemoryDataStore.cs` — seed more data
 `site.css` — adjust styling
 `_Layout.cshtml` — modify layout/navigation



 🧼 Resetting Data

Because this app uses in-memory storage:

 Data resets automatically every time the app restarts.
 Great for demos, training, or isolated environments.



 📄 License

MIT License – Free to use and modify.



