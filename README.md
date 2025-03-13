# Business Model Canvas (HTML/CSS Implementation)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Business Model Canvas</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --accent-color: #2980b9;
            --text-color: #333;
            --border-color: #bdc3c7;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background: #ecf0f1;
            padding: 2rem;
            min-height: 100vh;
        }

        .canvas-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-auto-rows: minmax(200px, auto);
            gap: 1rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .bmc-section {
            background: white;
            border: 2px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .section-header {
            color: var(--primary-color);
            font-weight: 600;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent-color);
        }

        .section-content {
            font-size: 0.95rem;
            line-height: 1.6;
            color: var(--text-color);
        }

        #value-propositions {
            grid-column: 2 / 3;
            grid-row: 2 / 4;
            min-height: 300px;
        }

        .export-btn {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background: var(--accent-color);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .export-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 3px 8px rgba(0,0,0,0.2);
        }

        @media (max-width: 768px) {
            .canvas-grid {
                grid-template-columns: 1fr;
            }
            
            #value-propositions {
                grid-column: 1;
                grid-row: auto;
                min-height: auto;
            }
            
            body {
                padding: 1rem;
            }
        }

        @media print {
            body {
                background: white;
                padding: 0.5in;
            }
            
            .bmc-section {
                box-shadow: none;
                page-break-inside: avoid;
            }
            
            .export-btn {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="canvas-grid">
        <!-- Row 1 -->
        <div class="bmc-section">
            <div class="section-header">Key Partners</div>
            <div class="section-content">
                • Strategic alliances<br>
                • Supplier network<br>
                • Technology partners<br>
                • Distribution partners
            </div>
        </div>
        
        <div class="bmc-section">
            <div class="section-header">Key Activities</div>
            <div class="section-content">
                • Product development<br>
                • Customer acquisition<br>
                • Operations management<br>
                • Strategic partnerships
            </div>
        </div>
        
        <div class="bmc-section">
            <div class="section-header">Key Resources</div>
            <div class="section-content">
                • Intellectual property<br>
                • Skilled team<br>
                • Technology stack<br>
                • Financial capital
            </div>
        </div>

        <!-- Value Propositions (Center) -->
        <div class="bmc-section" id="value-propositions">
            <div class="section-header">Value Propositions</div>
            <div class="section-content">
                • Innovative solutions<br>
                • Cost efficiency<br>
                • Superior quality<br>
                • Customization options
            </div>
        </div>

        <!-- Customer Relationships -->
        <div class="bmc-section">
            <div class="section-header">Customer Relationships</div>
            <div class="section-content">
                • Personal account management<br>
                • Self-service portal<br>
                • 24/7 support<br>
                • Community engagement
            </div>
        </div>
        
        <!-- Channels -->
        <div class="bmc-section">
            <div class="section-header">Channels</div>
            <div class="section-content">
                • Direct sales<br>
                • Online platform<br>
                • Partner network<br>
                • Mobile application
            </div>
        </div>

        <!-- Customer Segments -->
        <div class="bmc-section">
            <div class="section-header">Customer Segments</div>
            <div class="section-content">
                • Enterprise clients<br>
                • SMBs<br>
                • Individual consumers<br>
                • Government agencies
            </div>
        </div>

        <!-- Cost Structure -->
        <div class="bmc-section">
            <div class="section-header">Cost Structure</div>
            <div class="section-content">
                • R&D expenses<br>
                • Marketing costs<br>
                • Operations<br>
                • Staffing<br>
                • Technology infrastructure
            </div>
        </div>
        
        <!-- Revenue Streams -->
        <div class="bmc-section">
            <div class="section-header">Revenue Streams</div>
            <div class="section-content">
                • Subscription model<br>
                • Licensing fees<br>
                • Consulting services<br>
                • Premium features
            </div>
        </div>
    </div>

    <button class="export-btn" onclick="window.print()">Export PDF</button>
</body>
</html>
