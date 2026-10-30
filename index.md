HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.2 — Pricing Cards & Centered Login Form</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="pricing-style.css">
</head>
<body>

    <!-- Header -->
    <header class="page-header">
        <h1>Flexbox Layout Showcase</h1>
        <p>Exploring aligned pricing cards and perfectly centered form containers.</p>
    </header>

    <main class="main-container">
        
        <!-- --- SECTION 1: PRICING CARDS --- -->
        <section class="pricing-section">
            <h2>Choose Your Plan</h2>
            <p class="section-desc">Flexible pricing options built for developers and teams.</p>

            <!-- Flexbox Pricing Cards Container -->
            <div class="pricing-wrapper">
                
                <!-- Basic Card -->
                <div class="price-card">
                    <h3>Basic</h3>
                    <div class="price"><strong>$0</strong><span> / month</span></div>
                    <ul class="features-list">
                        <li>1 User Account</li>
                        <li>Basic Community Access</li>
                        <li>Standard Support</li>
                    </ul>
                    <button class="card-btn">Get Started</button>
                </div>

                <!-- Pro Card (Featured) -->
                <div class="price-card pro-card">
                    <span class="badge">Popular</span>
                    <h3>Pro</h3>
                    <div class="price"><strong>$19</strong><span> / month</span></div>
                    <ul class="features-list">
                        <li>5 User Accounts</li>
                        <li>Advanced Workshops</li>
                        <li>Priority Email Support</li>
                    </ul>
                    <button class="card-btn pro-btn">Choose Pro</button>
                </div>

                <!-- Premium Card -->
                <div class="price-card">
                    <h3>Premium</h3>
                    <div class="price"><strong>$49</strong><span> / month</span></div>
                    <ul class="features-list">
                        <li>Unlimited Users</li>
                        <li>All Access Modules</li>
                        <li>24/7 Dedicated Support</li>
                    </ul>
                    <button class="card-btn">Go Premium</button>
                </div>

            </div>
        </section>

        <!-- --- SECTION 2: CENTERED LOGIN FORM --- -->
        <section class="login-section">
            <h2>Member Login</h2>
            <p class="section-desc">Sign in to your account to manage your subscription.</p>

            <!-- Centered Flex Container for Login Form -->
            <div class="login-container">
                <form class="login-form" action="#" method="POST">
                    
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email" placeholder="student@example.com" required>
                    </div>

                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" name="password" placeholder="••••••••" required>
                    </div>

                    <button type="submit" class="login-btn">Sign In</button>

                </form>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Student Flexbox Lab. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: pricing-style.css
CSS
/* --- Global Reset & Typography --- */
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

/* --- Page Header --- */
.page-header {
    background-color: #0f172a;
    color: #ffffff;
    text-align: center;
    padding: 3rem 1rem;
}

.page-header h1 {
    font-size: 2.2rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    color: #94a3b8;
}

/* --- Main Layout Container --- */
.main-container {
    max-width: 1100px;
    margin: 3rem auto;
    padding: 0 1.5rem;
}

.section-desc {
    text-align: center;
    color: #64748b;
    margin-bottom: 2.5rem;
}

/* ==========================================
   PRICING CARDS SECTION (Flexbox)
   ================================---------- */
.pricing-section {
    margin-bottom: 5rem;
}

.pricing-section h2 {
    text-align: center;
    color: #1e293b;
    font-size: 1.8rem;
    margin-bottom: 0.5rem;
}

/* Flexbox Parent Container for Pricing Cards */
.pricing-wrapper {
    display: flex;                  /* Enable Flexbox */
    justify-content: center;        /* Center cards horizontally */
    align-items: stretch;           /* Make cards equal height */
    flex-wrap: wrap;                /* Wrap cards on smaller screens */
    gap: 2rem;                      /* Spacing between cards */
}

/* Individual Pricing Card */
.price-card {
    position: relative;
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 2.5rem 2rem;
    width: 100%;
    max-width: 320px;
    display: flex;
    flex-direction: column;         /* Stack content vertically inside card */
    justify-content: space-between;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.03);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.price-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.08);
}

/* Highlighted Pro Card */
.pro-card {
    border: 2px solid #2563eb;
    background-color: #eff6ff;
}

.badge {
    position: absolute;
    top: -12px;
    right: 20px;
    background-color: #2563eb;
    color: #ffffff;
    font-size: 0.75rem;
    font-weight: 700;
    padding: 0.25rem 0.75rem;
    border-radius: 50px;
    text-transform: uppercase;
}

.price-card h3 {
    font-size: 1.3rem;
    color: #1e293b;
    margin-bottom: 0.5rem;
}

.price {
    font-size: 2.2rem;
    color: #0f172a;
    margin-bottom: 1.5rem;
}

.price span {
    font-size: 0.9rem;
    font-weight: 400;
    color: #64748b;
}

.features-list {
    list-style: none;
    margin-bottom: 2rem;
}

.features-list li {
    padding: 0.5rem 0;
    border-bottom: 1px solid #e2e8f0;
    color: #475569;
    font-size: 0.95rem;
}

.card-btn {
    width: 100%;
    padding: 0.75rem;
    background-color: #334155;
    color: #ffffff;
    font-weight: 600;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.card-btn:hover {
    background-color: #1e293b;
}

.pro-btn {
    background-color: #2563eb;
}

.pro-btn:hover {
    background-color: #1d4ed8;
}


/* ==========================================
   CENTERED LOGIN FORM SECTION
   ================================---------- */
.login-section h2 {
    text-align: center;
    color: #1e293b;
    font-size: 1.8rem;
    margin-bottom: 0.5rem;
}

/* Flexbox Parent Container for Centering Login Form */
.login-container {
    display: flex;                  /* Enable Flexbox */
    justify-content: center;        /* Center horizontally */
    align-items: center;            /* Center vertically */
    min-height: 350px;              /* Ensures vertical centering space */
}

/* Login Form Box */
.login-form {
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 2.5rem;
    width: 100%;
    max-width: 400px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.03);
    
    /* Using flex-direction column to stack form elements vertically */
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
}

.form-group label {
    font-weight: 600;
    font-size: 0.9rem;
    color: #334155;
}

.form-group input {
    padding: 0.75rem;
    border: 1px solid #cbd5e1;
    border-radius: 6px;
    font-size: 1rem;
    outline: none;
    transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.form-group input:focus {
    border-color: #2563eb;
    box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.15);
}

.login-btn {
    background-color: #0f172a;
    color: #ffffff;
    padding: 0.75rem;
    font-size: 1rem;
    font-weight: 600;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.2s ease;
    margin-top: 0.5rem;
}

.login-btn:hover {
    background-color: #1e293b;
}

/* --- Footer --- */
footer {
    text-align: center;
    padding: 2rem;
    background-color: #0f172a;
    color: #94a3b8;
    font-size: 0.9rem;
    margin-top: 4rem;
}