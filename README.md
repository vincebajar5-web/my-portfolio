<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name="description" content="Personal portfolio showcasing programming projects, certificates, and skills." />
<title>My Portfolio</title>
<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  html {
    scroll-behavior: smooth;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #89f7fe 0%, #66a6ff 100%);
    color: #222;
    line-height: 1.6;
  }
  header {
    background: #1e3c72;
    background: linear-gradient(90deg, #2a5298 0%, #1e3c72 100%);
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 8px rgba(0,0,0,0.15);
  }
  nav {
    max-width: 960px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .site-title {
    font-weight: 900;
    font-size: 1.25rem;
    color: #fff;
    letter-spacing: 1.2px;
    text-decoration: none;
    text-shadow: 1px 1px 4px rgba(0,0,0,0.3);
  }
  .nav-links {
    list-style: none;
    display: flex;
    gap: 2rem;
  }
  .nav-links a {
    text-decoration: none;
    color: #d0e6ff;
    font-weight: 600;
    transition: color 0.3s ease;
  }
  .nav-links a:hover {
    color: #ffd700;
  }
  main {
    max-width: 960px;
    margin: 2rem auto;
    background: #fff;
    border-radius: 10px;
    padding: 2rem 2.5rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
  }
  section {
    padding: 3rem 0;
    border-bottom: 2px solid #f0f0f0;
  }
  section:last-of-type {
    border-bottom: none;
  }
  h1 {
    font-size: 3rem;
    color: #323232;
    margin-bottom: 1rem;
    text-shadow: 1px 1px 3px #aaa;
  }
  h2 {
    font-size: 2rem;
    color: #444;
    margin-bottom: 1.5rem;
    border-left: 6px solid #66a6ff;
    padding-left: 12px;
  }
  h3 {
    font-size: 1.25rem;
    color: #555;
    margin-bottom: 0.75rem;
  }
  p, .subtitle {
    color: #555;
    font-size: 1.1rem;
    max-width: 700px;
    margin-bottom: 1.4rem;
  }
  .subtitle {
    font-weight: 500;
    font-style: italic;
  }
  .button {
    display: inline-block;
    background: #66a6ff;
    color: #fff;
    padding: 0.75rem 1.5rem;
    border-radius: 30px;
    font-size: 1rem;
    font-weight: 700;
    text-decoration: none;
    box-shadow: 0 6px 12px rgba(102,166,255,0.4);
    transition: background 0.3s ease, transform 0.3s ease;
    border: none;
    cursor: pointer;
  }
  .button:hover {
