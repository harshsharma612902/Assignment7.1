The HTML File (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Header containing a logo, navigation links, and a button -->
    <header class="site-header">
        <div class="nav-container">
            <div class="logo">
                <a href="#home">DevBrand</a>
            </div>

            <nav>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#about">About</a></li>
                </ul>
            </nav>

            <div class="nav-action">
                <a href="#get-started" class="btn-primary">Get Started</a>
            </div>
        </div>
    </header>

    <main style="padding: 40px; text-align: center;">
        <h1>Resize Your Browser Window</h1>
        <p>Drag the edge of your browser window to test how the Flexbox layout handles screen width changes.</p>
    </main>

</body>
</html>
2. The CSS File (style.css)
CSS
/* Global Reset & Typography */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
}

/* Header & Flexbox Container Layout */
.site-header {
    background-color: #ffffff;
    border-bottom: 1px solid #e2e8f0;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 16px 24px;
    
    /* Step 2: Apply display: flex */
    display: flex;
    
    /* Step 3: Space items out across the row */
    justify-content: space-between;
    
    /* Step 4: Align items vertically in the center */
    align-items: center;
}

/* Logo Styling */
.logo a {
    font-size: 1.25rem;
    font-weight: 800;
    color: #1e293b;
    text-decoration: none;
    letter-spacing: -0.5px;
}

/* Navigation Links List */
.nav-links {
    list-style: none;
    display: flex;
    gap: 32px; /* Consistent spacing between links */
}

.nav-links a {
    text-decoration: none;
    color: #64748b;
    font-weight: 600;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

/* Step 5: Hover effect for links */
.nav-links a:hover {
    color: #3b82f6;
}

/* Step 5: Button Styling */
.btn-primary {
    background-color: #3b82f6;
    color: #ffffff;
    padding: 10px 20px;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.95rem;
    transition: background-color 0.2s ease, transform 0.1s ease;
    display: inline-block;
}

.btn-primary:hover {
    background-color: #2563eb;
}

.btn-primary:active {
    transform: scale(0.98);
}

/* Step 6: Responsive check media query (Optional enhancement) */
@media (max-width: 768px) {
    .nav-links {
        display: none; /* Can be paired with a mobile hamburger menu later */
    }
}