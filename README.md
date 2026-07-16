# Responsive-HTML-CSS-Landing-Page
index1.html
A modern responsive website template built with HTML5 and CSS3 using Flexbox, CSS Grid, and media queries. Features a responsive header, hero section, card-based content, information blocks, and footer without any frameworks.
Bootstrap 5 Grid System
desc for this

this is index2.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Bootstrap Grid Layout | Responsive Containers, Rows & Columns</title>
    <!-- Bootstrap 5 CSS + Icons -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <!-- Google Fonts for clean typography -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif;
            background: #f1f5f9;
            color: #0f172a;
            scroll-behavior: smooth;
        }

        /* Demo styling for grid cells */
        .demo-box {
            background: linear-gradient(145deg, #ffffff, #f8fafc);
            border-radius: 1rem;
            padding: 1.5rem 0.75rem;
            text-align: center;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            transition: all 0.2s ease;
            height: 100%;
        }

        .demo-box:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 20px -12px rgba(0, 0, 0, 0.15);
            border-color: #cbd5e1;
        }

        .bg-primary-light {
            background: linear-gradient(135deg, #e0f2fe, #bae6fd);
            border-left: 4px solid #0ea5e9;
        }

        .bg-success-light {
            background: linear-gradient(135deg, #dcfce7, #bbf7d0);
            border-left: 4px solid #22c55e;
        }

        .bg-warning-light {
            background: linear-gradient(135deg, #fef9c3, #fef08a);
            border-left: 4px solid #eab308;
        }

        .bg-purple-light {
            background: linear-gradient(135deg, #f3e8ff, #e9d5ff);
            border-left: 4px solid #a855f7;
        }

        .section-title {
            font-weight: 700;
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 3px solid #0ea5e9;
            display: inline-block;
        }

        .grid-demo-container {
            background: #ffffffcc;
            border-radius: 1.5rem;
            padding: 1.2rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
        }

        .code-note {
            background: #1e293b;
            color: #e2e8f0;
            padding: 0.5rem 1rem;
            border-radius: 12px;
            font-family: 'SF Mono', monospace;
            font-size: 0.75rem;
            margin-top: 0.8rem;
        }

        footer {
            background: #0f172a;
            color: #94a3b8;
            padding: 2rem 0;
            margin-top: 3rem;
        }

        hr {
            opacity: 0.3;
        }
    </style>
</head>
<body>

<!-- Header / Hero -->
<section class="container-fluid bg-dark text-white py-4 mb-4">
    <div class="container">
        <h1 class="display-6 fw-bold"><i class="bi bi-grid-3x3-gap-fill me-2"></i> Bootstrap 5 Grid System</h1>
        <p class="lead">Fully responsive layout using containers, rows, and columns — breakpoints from xs to xxl</p>
    </div>
</section>

<div class="container my-4">
    <!-- ========== SECTION 1: BASIC EQUAL COLUMNS ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-layout-three-columns me-2"></i> 1. Equal-width Columns (Auto-layout)</h2>
        <p class="text-muted">Three equal columns across all breakpoints using <code>.col</code> inside a row.</p>
        <div class="row g-4 mt-2">
            <div class="col">
                <div class="demo-box bg-primary-light">
                    <i class="bi bi-phone fs-1"></i>
                    <h5 class="mt-2">.col</h5>
                    <p class="small mb-0">Column 1 — Auto width</p>
                </div>
            </div>
            <div class="col">
                <div class="demo-box bg-primary-light">
                    <i class="bi bi-laptop fs-1"></i>
                    <h5 class="mt-2">.col</h5>
                    <p class="small mb-0">Column 2 — Flexible</p>
                </div>
            </div>
            <div class="col">
                <div class="demo-box bg-primary-light">
                    <i class="bi bi-tablet fs-1"></i>
                    <h5 class="mt-2">.col</h5>
                    <p class="small mb-0">Column 3 — Equal</p>
                </div>
            </div>
        </div>
        <div class="code-note">
            <i class="bi bi-code-slash me-1"></i> &lt;div class="row"&gt; &lt;div class="col"&gt;...&lt;/div&gt; &lt;div class="col"&gt;...&lt;/div&gt; &lt;div class="col"&gt;...&lt;/div&gt; &lt;/div&gt;
        </div>
    </div>

    <!-- ========== SECTION 2: RESPONSIVE BREAKPOINTS (Mobile first) ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-arrows-expand me-2"></i> 2. Responsive Columns (Breakpoints)</h2>
        <p class="text-muted">Columns stack on mobile, become horizontal on medium screens and above: <code>col-md-4</code></p>
        <div class="row g-4 mt-2">
            <div class="col-12 col-md-4">
                <div class="demo-box bg-success-light">
                    <i class="bi bi-box-seam fs-1"></i>
                    <h5>col-12 col-md-4</h5>
                    <p class="small">Full width on mobile → 1/3 on tablet/desktop</p>
                </div>
            </div>
            <div class="col-12 col-md-4">
                <div class="demo-box bg-success-light">
                    <i class="bi bi-bar-chart-steps fs-1"></i>
                    <h5>col-12 col-md-4</h5>
                    <p class="small">Adapts to viewport: responsive grid</p>
                </div>
            </div>
            <div class="col-12 col-md-4">
                <div class="demo-box bg-success-light">
                    <i class="bi bi-grid-3x3-gap fs-1"></i>
                    <h5>col-12 col-md-4</h5>
                    <p class="small">Perfect for card layouts</p>
                </div>
            </div>
        </div>
        <div class="row g-4 mt-2">
            <div class="col-6 col-lg-3">
                <div class="demo-box bg-warning-light">
                    <i class="bi bi-phone-landscape fs-1"></i>
                    <h6>col-6 col-lg-3</h6>
                    <small>2 cols on mobile, 4 cols on large</small>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="demo-box bg-warning-light">
                    <i class="bi bi-watch fs-1"></i>
                    <h6>col-6 col-lg-3</h6>
                    <small>Responsive breakpoint demo</small>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="demo-box bg-warning-light">
                    <i class="bi bi-camera fs-1"></i>
                    <h6>col-6 col-lg-3</h6>
                    <small>Flexible grid behavior</small>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="demo-box bg-warning-light">
                    <i class="bi bi-speaker fs-1"></i>
                    <h6>col-6 col-lg-3</h6>
                    <small>Stacking at different widths</small>
                </div>
            </div>
        </div>
        <div class="code-note">
            <i class="bi bi-grid"></i> .col-12 (xs), .col-md-4 (≥768px), .col-lg-3 (≥992px) — fully responsive
        </div>
    </div>

    <!-- ========== SECTION 3: NESTED ROWS & COLUMNS ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-diagram-3 me-2"></i> 3. Nested Grids (Rows inside Columns)</h2>
        <p class="text-muted">Columns can contain their own row and column structure for complex layouts.</p>
        <div class="row g-4 mt-2">
            <div class="col-md-6">
                <div class="demo-box bg-purple-light" style="background: #f5f3ff;">
                    <h5><i class="bi bi-folder2-open"></i> Parent Column A</h5>
                    <p>This column contains a nested grid (inner row).</p>
                    <div class="row g-2 mt-2">
                        <div class="col-6">
                            <div class="bg-white rounded p-2 border">Nested .col-6</div>
                        </div>
                        <div class="col-6">
                            <div class="bg-white rounded p-2 border">Nested .col-6</div>
                        </div>
                        <div class="col-12">
                            <div class="bg-white rounded p-2 border">Nested full width .col-12</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="demo-box bg-purple-light" style="background: #faf5ff;">
                    <h5><i class="bi bi-layers"></i> Parent Column B</h5>
                    <p>Another column with nested 3 equal columns inside.</p>
                    <div class="row g-2 mt-2">
                        <div class="col-4">
                            <div class="bg-white rounded p-2 text-center border">1</div>
                        </div>
                        <div class="col-4">
                            <div class="bg-white rounded p-2 text-center border">2</div>
                        </div>
                        <div class="col-4">
                            <div class="bg-white rounded p-2 text-center border">3</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="code-note">
            <i class="bi bi-braces"></i> Nesting: .row inside .col creates independent grid context without breaking parent.
        </div>
    </div>

    <!-- ========== SECTION 4: OFFSETTING & ORDERING ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-arrow-left-right me-2"></i> 4. Offsetting & Column Ordering</h2>
        <p class="text-muted">Using <code>.offset-*</code> and <code>.order-*</code> classes for flexible positioning.</p>
        <div class="row g-3 mb-4">
            <div class="col-md-4 offset-md-2">
                <div class="demo-box" style="background:#d9f0ff;">
                    <i class="bi bi-arrow-right-circle"></i> <strong>.col-md-4 .offset-md-2</strong>
                    <p class="small mb-0">Pushed by 2 columns on medium+</p>
                </div>
            </div>
            <div class="col-md-4">
                <div class="demo-box" style="background:#d9f0ff;">
                    <i class="bi bi-arrow-left-circle"></i> <strong>.col-md-4</strong>
                    <p class="small mb-0">Normal column</p>
                </div>
            </div>
        </div>
        <div class="row g-3">
            <div class="col order-last order-md-first">
                <div class="demo-box bg-primary-light">
                    <span class="badge bg-secondary mb-2">Order 1 (on mobile last)</span>
                    <p><code>.order-last .order-md-first</code></p>
                </div>
            </div>
            <div class="col order-first order-md-last">
                <div class="demo-box bg-primary-light">
                    <span class="badge bg-secondary mb-2">Order 2 (on mobile first)</span>
                    <p><code>.order-first .order-md-last</code></p>
                </div>
            </div>
            <div class="col">
                <div class="demo-box bg-primary-light">
                    <span class="badge bg-secondary mb-2">Default order</span>
                    <p>Natural flow</p>
                </div>
            </div>
        </div>
        <div class="code-note mt-3">
            <i class="bi bi-sort-numeric-down"></i> Offsetting moves columns to right; Order classes rearrange content responsively.
        </div>
    </div>

    <!-- ========== SECTION 5: VARIABLE WIDTH CONTENT (AUTO LAYOUT) ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-aspect-ratio me-2"></i> 5. Variable Width & Auto-sizing</h2>
        <p class="text-muted">Use <code>.col-auto</code> for columns that shrink to fit content width.</p>
        <div class="row g-3 align-items-center justify-content-center">
            <div class="col-auto">
                <div class="demo-box px-4" style="background:#ffe4e6;">
                    <i class="bi bi-envelope-paper fs-4"></i> .col-auto
                </div>
            </div>
            <div class="col">
                <div class="demo-box" style="background:#ffe4e6;">
                    <i class="bi bi-fill"></i> .col (fills remaining space)
                </div>
            </div>
            <div class="col-auto">
                <div class="demo-box px-4" style="background:#ffe4e6;">
                    <i class="bi bi-bell fs-4"></i> .col-auto
                </div>
            </div>
        </div>
        <div class="row g-3 mt-2">
            <div class="col-lg-2 col-md-3 col-6">
                <div class="demo-box">col-6 col-md-3 col-lg-2</div>
            </div>
            <div class="col-lg-2 col-md-3 col-6">
                <div class="demo-box">col-6 col-md-3 col-lg-2</div>
            </div>
            <div class="col-lg-2 col-md-3 col-6">
                <div class="demo-box">col-6 col-md-3 col-lg-2</div>
            </div>
            <div class="col-lg-2 col-md-3 col-6">
                <div class="demo-box">col-6 col-md-3 col-lg-2</div>
            </div>
            <div class="col-lg-2 col-md-6 col-6">
                <div class="demo-box">col-6 col-md-6 col-lg-2</div>
            </div>
            <div class="col-lg-2 col-md-6 col-12">
                <div class="demo-box">col-12 col-md-6 col-lg-2</div>
            </div>
        </div>
    </div>

    <!-- ========== SECTION 6: GUTTERS (GAP BETWEEN COLUMNS) ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-arrows-angle-expand me-2"></i> 6. Gutters (Spacing Control)</h2>
        <p class="text-muted">Adjust horizontal and vertical gutters using <code>.g-*</code> or <code>.gy-*</code>, <code>.gx-*</code>.</p>
        <div class="row g-1 mb-3">
            <div class="col-4">
                <div class="demo-box bg-secondary bg-opacity-10"><small>.g-1 (small gap)</small></div>
            </div>
            <div class="col-4">
                <div class="demo-box bg-secondary bg-opacity-10"><small>tight gutter</small></div>
            </div>
            <div class="col-4">
                <div class="demo-box bg-secondary bg-opacity-10"><small>minimal spacing</small></div>
            </div>
        </div>
        <div class="row g-5">
            <div class="col-md-6">
                <div class="demo-box" style="background:#e9f5ff;"><i class="bi bi-arrows-expand-vertical"></i> <strong>Large gutters (.g-5)</strong><br>More breathing space</div>
            </div>
            <div class="col-md-6">
                <div class="demo-box" style="background:#e9f5ff;"><i class="bi bi-arrows-expand"></i> <strong>Responsive gutters</strong><br>Customizable via breakpoints</div>
            </div>
        </div>
        <div class="code-note">
            <i class="bi bi-sliders2"></i> Gutter classes: .g-0, .g-2, .g-4, .g-5 — also row-cols for automatic column wrapping.
        </div>
    </div>

    <!-- ========== SECTION 7: ROW COLUMNS (AUTOMATIC WRAPPING) ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-columns-gap me-2"></i> 7. Row Columns (.row-cols-*)</h2>
        <p class="text-muted">Define how many columns per row without adding individual column classes.</p>
        <div class="row row-cols-2 row-cols-sm-3 row-cols-md-4 row-cols-lg-5 g-3">
            <div class="col"><div class="demo-box text-center">Item 1</div></div>
            <div class="col"><div class="demo-box text-center">Item 2</div></div>
            <div class="col"><div class="demo-box text-center">Item 3</div></div>
            <div class="col"><div class="demo-box text-center">Item 4</div></div>
            <div class="col"><div class="demo-box text-center">Item 5</div></div>
            <div class="col"><div class="demo-box text-center">Item 6</div></div>
            <div class="col"><div class="demo-box text-center">Item 7</div></div>
            <div class="col"><div class="demo-box text-center">Item 8</div></div>
            <div class="col"><div class="demo-box text-center">Item 9</div></div>
        </div>
        <div class="code-note mt-3">
            <i class="bi bi-layout-split"></i> .row-cols-2 (2 cols on mobile) → .row-cols-md-4 (4 cols on medium screens)
        </div>
    </div>

    <!-- ========== SECTION 8: CONTAINER FLUID & BREAKPOINTS ========== -->
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-border-width me-2"></i> 8. Container Variants</h2>
        <p>Bootstrap offers <code>.container</code> (fixed max-width at each breakpoint), <code>.container-fluid</code> (full width), and <code>.container-{breakpoint}</code>.</p>
        <div class="bg-dark text-white p-3 rounded mb-2">
            <strong>Current demo:</strong> This entire layout uses <code>.container</code> (responsive padding & max-width).
        </div>
        <div class="container-fluid bg-light p-3 rounded border mt-2">
            <small class="text-muted">📌 Example of nested container-fluid (full width inner section). The main grid is inside a standard container for elegance.</small>
        </div>
    </div>
</div>

<!-- Alignment & utilities showcase (extra) -->
<div class="container mb-5">
    <div class="grid-demo-container">
        <h2 class="section-title"><i class="bi bi-align-center me-2"></i> 9. Vertical & Horizontal Alignment</h2>
        <div class="row align-items-center g-3" style="min-height: 160px; background: #f8fafc; border-radius: 1rem; padding: 1rem;">
            <div class="col-4">
                <div class="demo-box bg-opacity-25">Aligned center (row align-items-center)</div>
            </div>
            <div class="col-4">
                <div class="demo-box bg-opacity-25">Flexible row alignment</div>
            </div>
            <div class="col-4">
                <div class="demo-box bg-opacity-25">Using .align-items-center</div>
            </div>
        </div>
        <div class="row justify-content-between mt-4 g-2">
            <div class="col-md-3">
                <div class="demo-box">.justify-content-between</div>
            </div>
            <div class="col-md-3">
                <div class="demo-box">Space between columns</div>
            </div>
            <div class="col-md-3">
                <div class="demo-box">Flexible distribution</div>
            </div>
        </div>
    </div>
</div>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="row">
            <div class="col-md-8">
                <h5><i class="bi bi-bootstrap-fill me-2"></i> Bootstrap 5 Responsive Grid</h5>
                <p>Demonstrates containers, rows, columns, nesting, offsets, gutters, row-cols, and alignment utilities.<br>
                Fully responsive across all devices (xs, sm, md, lg, xl, xxl).</p>
            </div>
            <div class="col-md-4 text-md-end">
                <i class="bi bi-grid-3x3-gap-fill fs-2"></i>
                <p class="small mt-2">Built with modern CSS + Bootstrap 5.3</p>
            </div>
        </div>
        <hr class="my-3">
        <div class="text-center small">
            © 2025 — Responsive Grid Mastery | Resize browser to test breakpoints
        </div>
    </div>
</footer>

<!-- Bootstrap JS Bundle (optional for certain interactions, but grid works without) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>


index3.html

repsonsive gridsstem 3

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Responsive Website | Bootstrap Grid + Media Queries | Sidebar & Main Content</title>
    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Bootstrap Icons -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif;
            background: #f0f2f5;
            overflow-x: hidden;
        }

        /* ========== NAVBAR STYLES ========== */
        .navbar-custom {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            padding: 1rem 0;
        }

        .navbar-brand {
            font-weight: 800;
            font-size: 1.6rem;
            background: linear-gradient(135deg, #e94560, #ff6b6b);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .nav-link {
            color: #e0e0e0 !important;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .nav-link:hover {
            color: #e94560 !important;
            transform: translateY(-2px);
        }

        /* ========== SIDEBAR STYLES ========== */
        .sidebar {
            background: white;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            padding: 1.5rem;
            position: sticky;
            top: 20px;
            transition: all 0.3s ease;
        }

        .sidebar-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: #1a1a2e;
            margin-bottom: 1.5rem;
            padding-bottom: 0.75rem;
            border-bottom: 3px solid #e94560;
            display: inline-block;
        }

        .sidebar-menu {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .sidebar-menu li {
            margin-bottom: 0.75rem;
        }

        .sidebar-menu a {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.75rem 1rem;
            color: #4a5568;
            text-decoration: none;
            border-radius: 12px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .sidebar-menu a:hover {
            background: linear-gradient(135deg, #e94560, #ff6b6b);
            color: white;
            transform: translateX(5px);
        }

        .sidebar-menu a i {
            font-size: 1.2rem;
        }

        .sidebar-widget {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 1rem;
            margin-top: 1.5rem;
            text-align: center;
        }

        /* ========== MAIN CONTENT STYLES ========== */
        .main-content {
            background: white;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            padding: 2rem;
            transition: all 0.3s ease;
        }

        .hero-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 16px;
            padding: 2rem;
            color: white;
            margin-bottom: 2rem;
        }

        .hero-section h1 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: #1a1a2e;
            margin-bottom: 1.5rem;
            position: relative;
            padding-left: 1rem;
            border-left: 4px solid #e94560;
        }

        /* Card Styles */
        .content-card {
            background: #f8f9fa;
            border-radius: 16px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            height: 100%;
            border: 1px solid #e9ecef;
        }

        .content-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border-color: #e94560;
        }

        .content-card i {
            font-size: 2rem;
            color: #e94560;
            margin-bottom: 1rem;
        }

        .content-card h3 {
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 0.75rem;
        }

        /* Stats Section */
        .stat-box {
            text-align: center;
            padding: 1.5rem;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 16px;
            color: white;
            transition: transform 0.3s ease;
        }

        .stat-box:hover {
            transform: scale(1.05);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
        }

        .stat-label {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        /* Footer */
        .footer {
            background: #1a1a2e;
            color: #e0e0e0;
            padding: 3rem 0 1.5rem;
            margin-top: 3rem;
        }

        /* ========== CUSTOM MEDIA QUERIES (Beyond Bootstrap) ========== */
        
        /* Large Desktop Optimizations */
        @media (min-width: 1400px) {
            .container {
                max-width: 1320px;
            }
            
            .hero-section h1 {
                font-size: 2.5rem;
            }
            
            .stat-number {
                font-size: 3rem;
            }
        }
        
        /* Tablet Landscape to Desktop */
        @media (min-width: 992px) and (max-width: 1199px) {
            .sidebar {
                padding: 1.2rem;
            }
            
            .sidebar-menu a {
                padding: 0.6rem 0.8rem;
                font-size: 0.9rem;
            }
            
            .hero-section h1 {
                font-size: 1.8rem;
            }
        }
        
        /* Tablet Portrait (Medium devices) */
        @media (min-width: 768px) and (max-width: 991px) {
            .sidebar {
                margin-bottom: 1.5rem;
                position: relative;
                top: 0;
            }
            
            .hero-section {
                padding: 1.5rem;
            }
            
            .hero-section h1 {
                font-size: 1.6rem;
            }
            
            .main-content {
                padding: 1.5rem;
            }
            
            .stat-number {
                font-size: 1.8rem;
            }
        }
        
        /* Mobile Devices (Small screens) */
        @media (max-width: 767px) {
            .sidebar {
                margin-bottom: 1.5rem;
                position: relative;
                top: 0;
            }
            
            .main-content {
                padding: 1.2rem;
            }
            
            .hero-section {
                padding: 1.2rem;
                text-align: center;
            }
            
            .hero-section h1 {
                font-size: 1.4rem;
            }
            
            .section-title {
                font-size: 1.2rem;
            }
            
            .stat-number {
                font-size: 1.5rem;
            }
            
            .content-card {
                padding: 1rem;
            }
            
            .footer {
                text-align: center;
            }
        }
        
        /* Extra Small Devices */
        @media (max-width: 480px) {
            .hero-section h1 {
                font-size: 1.2rem;
            }
            
            .hero-section p {
                font-size: 0.9rem;
            }
            
            .sidebar-menu a {
                padding: 0.5rem 0.75rem;
                font-size: 0.85rem;
            }
            
            .stat-number {
                font-size: 1.2rem;
            }
            
            .stat-label {
                font-size: 0.7rem;
            }
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(135deg, #e94560, #ff6b6b);
            border-radius: 5px;
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .sidebar, .main-content {
            animation: fadeInUp 0.6s ease-out;
        }
        
        /* Card hover effects */
        .hover-lift {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .hover-lift:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <nav class="navbar navbar-expand-lg navbar-custom sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="bi bi-bootstrap-fill me-2"></i>ResponsiveGrid
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Portfolio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contact</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Main Container -->
    <div class="container my-4 my-md-5">
        <!-- Bootstrap Grid: Row with Sidebar + Main Content -->
        <div class="row g-4">
            
            <!-- ========== SIDEBAR SECTION (Left Column) ========== -->
            <div class="col-lg-4 col-md-12">
                <aside class="sidebar">
                    <h3 class="sidebar-title">
                        <i class="bi bi-grid-3x3-gap-fill me-2"></i>Dashboard
                    </h3>
                    
                    <!-- Sidebar Navigation Menu -->
                    <ul class="sidebar-menu">
                        <li><a href="#"><i class="bi bi-house-door-fill"></i> Overview</a></li>
                        <li><a href="#"><i class="bi bi-bar-chart-fill"></i> Analytics</a></li>
                        <li><a href="#"><i class="bi bi-people-fill"></i> Users</a></li>
                        <li><a href="#"><i class="bi bi-envelope-fill"></i> Messages</a></li>
                        <li><a href="#"><i class="bi bi-gear-fill"></i> Settings</a></li>
                        <li><a href="#"><i class="bi bi-bell-fill"></i> Notifications</a></li>
                    </ul>
                    
                    <!-- Sidebar Widget -->
                    <div class="sidebar-widget">
                        <i class="bi bi-megaphone-fill" style="font-size: 2rem; color: #e94560;"></i>
                        <h5 class="mt-2 mb-1">Pro Tip!</h5>
                        <p class="small mb-0">Use Bootstrap Grid + custom media queries for ultimate responsive control</p>
                    </div>
                    
                    <!-- Progress Stats -->
                    <div class="mt-4">
                        <h6 class="fw-bold mb-3">System Status</h6>
                        <div class="mb-2 d-flex justify-content-between">
                            <span>Storage</span>
                            <span class="small">68%</span>
                        </div>
                        <div class="progress mb-3" style="height: 8px;">
                            <div class="progress-bar bg-danger" style="width: 68%"></div>
                        </div>
                        <div class="mb-2 d-flex justify-content-between">
                            <span>Bandwidth</span>
                            <span class="small">45%</span>
                        </div>
                        <div class="progress mb-3" style="height: 8px;">
                            <div class="progress-bar bg-warning" style="width: 45%"></div>
                        </div>
                        <div class="mb-2 d-flex justify-content-between">
                            <span>CPU Usage</span>
                            <span class="small">32%</span>
                        </div>
                        <div class="progress" style="height: 8px;">
                            <div class="progress-bar bg-success" style="width: 32%"></div>
                        </div>
                    </div>
                </aside>
            </div>
            
            <!-- ========== MAIN CONTENT SECTION (Right Column) ========== -->
            <div class="col-lg-8 col-md-12">
                <main class="main-content">
                    
                    <!-- Hero Section -->
                    <div class="hero-section">
                        <h1>Welcome to Responsive Website</h1>
                        <p class="mb-0">Built with Bootstrap Grid System + Custom Media Queries featuring dynamic sidebar and main content layout that adapts beautifully across all devices.</p>
                    </div>
                    
                    <!-- Featured Content Section -->
                    <div class="row g-4 mb-5">
                        <div class="col-md-6">
                            <div class="content-card hover-lift">
                                <i class="bi bi-bootstrap-fill"></i>
                                <h3>Bootstrap Grid</h3>
                                <p class="small text-muted">12-column grid system with responsive breakpoints for seamless layouts across devices.</p>
                                <a href="#" class="text-decoration-none fw-bold" style="color: #e94560;">Learn More →</a>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="content-card hover-lift">
                                <i class="bi bi-phone-fill"></i>
                                <h3>Media Queries</h3>
                                <p class="small text-muted">Custom CSS media queries for fine-tuned control beyond Bootstrap defaults.</p>
                                <a href="#" class="text-decoration-none fw-bold" style="color: #e94560;">Learn More →</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Stats Section -->
                    <h3 class="section-title">Key Statistics</h3>
                    <div class="row g-3 mb-5">
                        <div class="col-md-3 col-6">
                            <div class="stat-box">
                                <div class="stat-number">1.2k+</div>
                                <div class="stat-label">Users</div>
                            </div>
                        </div>
                        <div class="col-md-3 col-6">
                            <div class="stat-box">
                                <div class="stat-number">350+</div>
                                <div class="stat-label">Projects</div>
                            </div>
                        </div>
                        <div class="col-md-3 col-6">
                            <div class="stat-box">
                                <div class="stat-number">24/7</div>
                                <div class="stat-label">Support</div>
                            </div>
                        </div>
                        <div class="col-md-3 col-6">
                            <div class="stat-box">
                                <div class="stat-number">98%</div>
                                <div class="stat-label">Satisfaction</div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Recent Activity Section -->
                    <h3 class="section-title">Recent Activity</h3>
                    <div class="list-group mb-4">
                        <div class="list-group-item list-group-item-action d-flex align-items-center gap-3 border-0 bg-light mb-2 rounded">
                            <i class="bi bi-person-plus-fill text-success fs-5"></i>
                            <div class="flex-grow-1">
                                <strong>New user registered</strong>
                                <p class="small text-muted mb-0">John Doe joined the platform</p>
                            </div>
                            <small class="text-muted">2 min ago</small>
                        </div>
                        <div class="list-group-item list-group-item-action d-flex align-items-center gap-3 border-0 bg-light mb-2 rounded">
                            <i class="bi bi-file-post-fill text-primary fs-5"></i>
                            <div class="flex-grow-1">
                                <strong>New content published</strong>
                                <p class="small text-muted mb-0">Responsive design tutorial</p>
                            </div>
                            <small class="text-muted">1 hour ago</small>
                        </div>
                        <div class="list-group-item list-group-item-action d-flex align-items-center gap-3 border-0 bg-light mb-2 rounded">
                            <i class="bi bi-star-fill text-warning fs-5"></i>
                            <div class="flex-grow-1">
                                <strong>Achievement unlocked</strong>
                                <p class="small text-muted mb-0">1000th registered user milestone</p>
                            </div>
                            <small class="text-muted">3 hours ago</small>
                        </div>
                    </div>
                    
                    <!-- Content Grid Demo -->
                    <h3 class="section-title">Latest Articles</h3>
                    <div class="row g-4">
                        <div class="col-md-4 col-sm-6">
                            <div class="content-card">
                                <img src="https://picsum.photos/id/20/300/150" alt="Article" class="img-fluid rounded mb-3" style="width: 100%; height: 120px; object-fit: cover;">
                                <h6 class="fw-bold">Understanding Bootstrap Grid</h6>
                                <p class="small text-muted">Learn how to leverage the power of 12-column grid system...</p>
                                <a href="#" class="text-decoration-none small fw-bold">Read more →</a>
                            </div>
                        </div>
                        <div class="col-md-4 col-sm-6">
                            <div class="content-card">
                                <img src="https://picsum.photos/id/26/300/150" alt="Article" class="img-fluid rounded mb-3" style="width: 100%; height: 120px; object-fit: cover;">
                                <h6 class="fw-bold">Media Queries Mastery</h6>
                                <p class="small text-muted">Custom breakpoints for pixel-perfect responsive design...</p>
                                <a href="#" class="text-decoration-none small fw-bold">Read more →</a>
                            </div>
                        </div>
                        <div class="col-md-4 col-sm-6">
                            <div class="content-card">
                                <img src="https://picsum.photos/id/1/300/150" alt="Article" class="img-fluid rounded mb-3" style="width: 100%; height: 120px; object-fit: cover;">
                                <h6 class="fw-bold">Sidebar Layout Best Practices</h6>
                                <p class="small text-muted">Optimize your sidebar + main content for all devices...</p>
                                <a href="#" class="text-decoration-none small fw-bold">Read more →</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Testimonial Section -->
                    <div class="alert alert-light border mt-4 p-4 rounded-4">
                        <div class="d-flex gap-3 align-items-start">
                            <i class="bi bi-quote fs-1" style="color: #e94560;"></i>
                            <div>
                                <p class="mb-2 fst-italic">"This responsive layout using Bootstrap Grid + custom media queries perfectly demonstrates how to create modern, adaptive websites that look great on any device."</p>
                                <strong>— Alex Morgan</strong>
                                <p class="small text-muted mb-0">Senior Web Developer</p>
                            </div>
                        </div>
                    </div>
                    
                </main>
            </div>
        </div>
    </div>
    
    <!-- ========== FOOTER SECTION ========== -->
    <footer class="footer">
        <div class="container">
            <div class="row g-4">
                <div class="col-md-4">
                    <h5 class="fw-bold mb-3" style="color: #e94560;">ResponsiveGrid</h5>
                    <p class="small">Building modern, responsive websites with Bootstrap 5 Grid system and custom media queries for optimal user experience across all devices.</p>
                    <div class="mt-3">
                        <a href="#" class="text-white me-3 opacity-75"><i class="bi bi-twitter-x"></i></a>
                        <a href="#" class="text-white me-3 opacity-75"><i class="bi bi-facebook"></i></a>
                        <a href="#" class="text-white me-3 opacity-75"><i class="bi bi-linkedin"></i></a>
                        <a href="#" class="text-white opacity-75"><i class="bi bi-github"></i></a>
                    </div>
                </div>
                <div class="col-md-2">
                    <h6 class="fw-bold mb-3">Product</h6>
                    <ul class="list-unstyled small">
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">Features</a></li>
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">Pricing</a></li>
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">Demo</a></li>
                    </ul>
                </div>
                <div class="col-md-2">
                    <h6 class="fw-bold mb-3">Company</h6>
                    <ul class="list-unstyled small">
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">About</a></li>
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">Blog</a></li>
                        <li class="mb-2"><a href="#" class="text-white-50 text-decoration-none">Careers</a></li>
                    </ul>
                </div>
                <div class="col-md-4">
                    <h6 class="fw-bold mb-3">Newsletter</h6>
                    <p class="small">Subscribe to get updates on responsive design tips</p>
                    <div class="input-group">
                        <input type="email" class="form-control form-control-sm" placeholder="Your email">
                        <button class="btn btn-danger btn-sm" type="button">Subscribe</button>
                    </div>
                </div>
            </div>
            <hr class="my-4 opacity-25">
            <div class="text-center small opacity-75">
                <p class="mb-0">&copy; 2025 ResponsiveGrid. Built with Bootstrap Grid + Custom Media Queries. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Bootstrap JS Bundle -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    
    <!-- Additional interactive script for responsive testing -->
    <script>
        // Log responsive breakpoint for debugging
        function logBreakpoint() {
            const width = window.innerWidth;
            let breakpoint = '';
            if (width < 576) breakpoint = 'Extra Small (xs)';
            else if (width < 768) breakpoint = 'Small (sm)';
            else if (width < 992) breakpoint = 'Medium (md)';
            else if (width < 1200) breakpoint = 'Large (lg)';
            else if (width < 1400) breakpoint = 'Extra Large (xl)';
            else breakpoint = 'XXL (xxl)';
            
            console.log(`Current viewport: ${width}px - ${breakpoint}`);
        }
        
        window.addEventListener('resize', () => {
            logBreakpoint();
        });
        
        logBreakpoint();
        
        // Add smooth scroll behavior
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
