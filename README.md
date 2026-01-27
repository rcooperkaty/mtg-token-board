<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Commander Token Board - User Guide</title>
  <style>
    :root {
      --bg-dark: #111;
      --bg-panel: #181818;
      --text-main: #eee;
      --text-muted: #aaa;
      --border: #333;
      --accent: #2f7d32;
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text-main);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      margin: 0;
      padding: 20px;
      line-height: 1.6;
    }

    .container {
      max-width: 800px;
      margin: 0 auto;
      background: var(--bg-panel);
      padding: 30px;
      border-radius: 12px;
      border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.5);
    }

    h1 {
      color: #fff;
      border-bottom: 2px solid var(--accent);
      padding-bottom: 10px;
      margin-top: 0;
    }

    h2 {
      color: var(--accent);
      margin-top: 30px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 5px;
    }

    h3 {
      color: #fff;
      margin-bottom: 5px;
    }

    p { margin-bottom: 15px; }

    ul, ol {
      margin-bottom: 20px;
      padding-left: 20px;
    }

    li { margin-bottom: 8px; }

    code {
      background: #333;
      padding: 2px 6px;
      border-radius: 4px;
      font-family: monospace;
      font-size: 0.9em;
    }

    /* Table Styling */
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 20px 0;
      background: #222;
      border-radius: 8px;
      overflow: hidden;
    }

    th, td {
      text-align: left;
      padding: 12px 15px;
      border-bottom: 1px solid var(--border);
    }

    th {
      background-color: #2a2a2a;
      color: var(--accent);
      font-weight: bold;
      text-transform: uppercase;
      font-size: 0.85em;
      letter-spacing: 1px;
    }

    tr:last-child td { border-bottom: none; }

    /* Icons and Badges */
    .icon { font-weight: bold; font-size: 1.2em; display: inline-block; vertical-align: middle; }
    
    .badge-zzz {
      background: rgba(180,180,0,0.2);
      border: 1px solid yellow;
      color: #ff9;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.8em;
      font-weight: bold;
    }

    /* Mobile optimization */
    @media (max-width: 600px) {
      .container { padding: 15px; }
      h1 { font-size: 1.5em; }
    }
  </style>
</head>
<body>

<div class="container">

  <h1>Commander Token Board Guide</h1>
  <p><strong>Commander Token Board</strong> is a lightweight, mobile-optimized web application designed to help Magic: The Gathering players manage complex board states without needing physical cards or dice.</p>

  <h2>📱 Installation (iOS & Android)</h2>
  <p>For the best experience, install this app to your home screen. This removes the browser address bar and runs the app in full-screen mode.</p>
  <ol>
    <li>Open the website
