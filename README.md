<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GemDistrict Art - Responsive Showcase</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Your existing CSS here */
    </style>
</head>
<body>
    <!-- Your existing HTML here -->
    
    <script>
        // Fixed mobile navigation
        const menuToggle = document.getElementById('menuToggle');
        const mobileNav = document.getElementById('mobileNav');
        const mobileNavClose = document.getElementById('mobileNavClose');
        
        menuToggle.addEventListener('click', () => {
            mobileNav.classList.add('open');
            document.body.style.overflow = 'hidden';
        });
        
        mobileNavClose.addEventListener('click', () => {
            mobileNav.classList.remove('open');
            document.body.style.overflow = 'auto';
        });
        
        // Fixed theme toggle
        const themeToggle = document.getElementById('themeToggle');
        const mobileThemeToggle = document.getElementById('mobileThemeToggle');
        const body = document.body;
        
        function toggleTheme() {
            body.classList.toggle('dark-mode');
            const icon = themeToggle.querySelector('i');
            const mobileIcon = mobileThemeToggle.querySelector('i');
            const text = themeToggle.querySelector('span');
            const mobileText = mobileThemeToggle.querySelector('span');
            
            if (body.classList.contains('dark-mode')) {
                icon.className = 'fas fa-sun';
                mobileIcon.className = 'fas fa-sun';
                text.textContent = 'Light Mode';
                mobileText.textContent = 'Light Mode';
            } else {
                icon.className = 'fas fa-moon';
                mobileIcon.className = 'fas fa-moon';
                text.textContent = 'Dark Mode';
                mobileText.textContent = 'Dark Mode';
            }
        }
        
        themeToggle.addEventListener('click', toggleTheme);
        mobileThemeToggle.addEventListener('click', toggleTheme);
        
        // Fixed AI identifier
        const uploadArea = document.getElementById('uploadArea');
        const identifyBtn = document.getElementById('identifyBtn');
        const resultDiv = document.getElementById('result');
        const gemResult = document.getElementById('gemResult');
        
        uploadArea.addEventListener('click', () => {
            // Simulate file selection
            const gemstones = ['Emerald', 'Ruby', 'Sapphire', 'Tourmaline', 'Lapis Lazuli', 'Alexandrite', 'Opal', 'Jade'];
            const randomGem = gemstones[Math.floor(Math.random() * gemstones.length)];
            gemResult.textContent = randomGem;
        });
        
        identifyBtn.addEventListener('click', () => 
