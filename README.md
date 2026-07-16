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
