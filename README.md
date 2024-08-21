<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OPD Dashboard</title>
    <link rel="stylesheet" href="../admin/css/bootstrap.min.css">
    <link rel="stylesheet" href="../admin/css/style.css">
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
            margin: 0;
            background-color: #f8f9fa;
        }

        .navbar {
            background-color: #343a40;
        }

        .navbar-brand .logo {
            display: flex;
            align-items: center;
        }

        .navbar-brand .logo h4 {
            margin-bottom: 0;
            color: #fff;
        }

        .navbar-brand .mehran {
            color: #fff;
            margin-left: 20px;
        }

        .navbar-nav .nav-link {
            color: #fff !important;
        }

        .navbar-nav .nav-link:hover {
            color: #ccc !important;
        }

        .dashboard-container {
            max-width: 1200px;
            width: 100%;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 15px rgb(0, 0, 0, 0.1);
            margin-top: 30px;
        }

        .dashboard-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .dashboard-stats {
            display: flex;
            justify-content: space-around;
            margin-bottom: 30px;
        }

        .stat-card {
            background-color: #007bff;
            color: white;
            padding: 20px;
            border-radius: 5px;
            width: 30%;
            text-align: center;
        }

        .stat-card h3 {
            margin: 0;
            font-size: 24px;
        }

        .appointments-section {
            margin-bottom: 30px;
        }

        .appointments-table {
            width: 100%;
            border-collapse: collapse;
        }

        .appointments-table th,
        .appointments-table td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        .appointments-table th {
            background-color: #007bff;
            color: white;
        }

        .doctors-section {
            margin-bottom: 30px;
        }

        .doctors-table {
            width: 100%;
            border-collapse: collapse;
        }

        .doctors-table th,
        .doctors-table td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        .doctors-table th {
            background-color: #007bff;
            color: white;
        }
    </style>
</head>

<body>
    <!-- Navigation Bar -->
    <section class="header">
        <nav class="navbar navbar-expand-lg bg-primary sticky-navbar">
            <div class="container-fluid">
                <a class="navbar-brand" href="#">
                    <img src="/static/images/delhi.png" alt="Delhi Logo" class="rounded-circle" width="40" height="40">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarColor01" aria-controls="navbarColor01" aria-expanded="false"
                    aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <h3 class="mehran">Government of NCT of Delhi</h3>
                <div class="collapse navbar-collapse" id="navbarColor01">
                    <ul class="navbar-nav ms-auto justify-content-end">
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/">Home</a>
                        </li>
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/#about">About Us</a>
                        </li>
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/#doctors">Doctors</a>
                        </li>
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/#departments">Departments</a>
                        </li>
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/#contact">Contact Us</a>
                        </li>
                        <li class="nav-item dropdown mr-3">
                            <a class="nav-link dropdown-toggle text-light" href="#" id="hospitalDropdown"
                                role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                Hospital
                            </a>
                            <ul class="dropdown-menu" aria-labelledby="hospitalDropdown">
                                <li><a class="dropdown-item" href="#">Opd</a></li>
                                <li><a class="dropdown-item" href="#">Medicines</a></li>
                                <li><a class="dropdown-item" href="#">Blood Bank</a></li>
                                <li><a class="dropdown-item" href="#">Bed Available</a></li>
                            </ul>
                        </li>
                        <li class="nav-item dropdown mr-3">
                            <a class="nav-link dropdown-toggle text-light" href="#" id="adminDropdown"
                                role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                Admin
                            </a>
                            <ul class="dropdown-menu" aria-labelledby="adminDropdown">
                                <li><a class="dropdown-item" href="/admin/dashboard.html">Dashboard</a></li>
                                <li><a class="dropdown-item" href="/admin/manage-users.html">Manage Patients</a></li>
                                <li><a class="dropdown-item" href="/admin/reports.html">Reports</a></li>
                                <li><a class="dropdown-item" href="/admin/settings.html">Settings</a></li>
                            </ul>
                        </li>
                        <li class="nav-item mr-3">
                            <a class="nav-link text-light" href="/templates/user login.html">Login</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </section>

    <!-- Dashboard Content -->
    <div class="container dashboard-container">
        <div class="dashboard-header">
            <h2>OPD Dashboard</h2>
        </div>
        <div class="dashboard-stats">
            <div class="stat-card">
                <h3>Patients Today</h3>
                <p>150</p>
            </div>
            <div class="stat-card">
                <h3>Available Doctors</h3>
                <p>20</p>
            </div>
            <div class="stat-card">
                <h3>Pending Appointments</h3>
                <p>45</p>
            </div>
        </div>

        <!-- Appointments Section -->
        <div class="appointments-section">
            <h4>Today's Appointments</h4>
            <table class="appointments-table">
                <thead>
                    <tr>
                        <th>Appointment ID</th>
                        <th>Patient Name</th>
                        <th>Doctor</th>
                        <th>Time</th>
                        <th>Status</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>1001</td>
                        <td>John Doe</td>
                        <td>Dr. Smith</td>
                        <td>10:00 AM</td>
                        <td>Pending</td>
                    </tr>
                    <tr>
                        <td>1002</td>
                        <td>Jane Doe</td>
                        <td>Dr. Adams</td>
                        <td>10:30 AM</td>
                        <td>Completed</td>
                    </tr>
                    <!-- Additional rows as needed -->
                </tbody>
            </table>
        </div>

        <!-- Doctors Section -->
        <div class="doctors-section">
            <h4>Available Doctors</h4>
            <table class="doctors-table">
                <thead>
                    <tr>
                        <th>Doctor ID</th>
                        <th>Doctor Name</th>
                        <th>Specialization</th>
                        <th>Availability</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>D001</td>
                        <td>Dr. Smith</td>
                        <td>Cardiology</td>
                        <td>Available</td>
                    </tr>
                    <tr>
                        <td>D002</td>
                        <td>Dr. Adams</td>
                        <td>Dermatology</td>
                        <td>Available</td>
                    </tr>
                    <!-- Additional rows as needed -->
                </tbody>
            </table>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
