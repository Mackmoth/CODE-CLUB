<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Code Club - Learn, Code, Create</title>
<script src="https://cdn.tailwindcss.com/3.4.16"></script>
<script>tailwind.config={theme:{extend:{colors:{primary:'#00FFFF',secondary:'#0000FF'},borderRadius:{'none':'0px','sm':'4px',DEFAULT:'8px','md':'12px','lg':'16px','xl':'20px','2xl':'24px','3xl':'32px','full':'9999px','button':'8px'}}}}</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/remixicon/4.6.0/remixicon.min.css">
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
body {
font-family: 'Inter', sans-serif;
scroll-behavior: smooth;
}
.floating-code {
animation: float 8s infinite ease-in-out;
opacity: 0.3;
position: absolute;
}
@keyframes float {
0% { transform: translateY(0) rotate(0deg); }
50% { transform: translateY(-20px) rotate(5deg); }
100% { transform: translateY(0) rotate(0deg); }
}
.glow-on-hover:hover {
box-shadow: 0 0 15px rgba(0, 255, 255, 0.7);
transition: all 0.3s ease;
}
.nav-link {
position: relative;
}
.nav-link::after {
content: '';
position: absolute;
width: 0;
height: 2px;
bottom: -4px;
left: 0;
background-color: #00FFFF;
transition: width 0.3s ease;
}
.nav-link:hover::after {
width: 100%;
}
.feature-card {
transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.feature-card:hover {
transform: translateY(-5px);
box-shadow: 0 10px 25px rgba(0, 255, 255, 0.2);
}
</style>
</head>
<body class="bg-white">
<!-- Navigation Bar -->
<nav class="fixed w-full top-0 z-50 bg-white bg-opacity-90 backdrop-blur-sm shadow-sm">
<div class="max-w-7xl mx-auto px-4">
<div class="flex justify-between h-16">
<div class="flex items-center">
<a href="#" class="flex items-center">
<img src="CODE.png" style="width:90px; height:90px;" alt="Code Club Logo" class="h-10">
</a>
</div>
<div class="hidden md:flex items-center space-x-8">
<a href="#" class="nav-link text-secondary font-medium cursor-pointer">Home</a>
<a href="#features" class="nav-link text-secondary font-medium cursor-pointer">Features</a>
<a href="#courses" class="nav-link text-secondary font-medium cursor-pointer">Courses</a>
<a href="#community" class="nav-link text-secondary font-medium cursor-pointer">Community</a>
<a href="#contact" class="nav-link text-secondary font-medium cursor-pointer">Contact</a>
<a href="#" class="bg-primary text-white px-5 py-2 !rounded-button font-medium hover:bg-opacity-90 transition-all cursor-pointer">Join Now</a>
</div>
<div class="md:hidden flex items-center">
<button id="mobile-menu-button" class="w-10 h-10 flex items-center justify-center cursor-pointer">
<i class="ri-menu-line ri-2x text-secondary"></i>
</button>
</div>
</div>
</div>
<!-- Mobile menu -->
<div id="mobile-menu" class="hidden md:hidden bg-white shadow-lg absolute w-full">
<div class="px-2 pt-2 pb-3 space-y-1">
<a href="#" class="block px-3 py-2 text-secondary font-medium hover:bg-primary hover:text-white !rounded-button cursor-pointer">Home</a>
<a href="#features" class="block px-3 py-2 text-secondary font-medium hover:bg-primary hover:text-white !rounded-button cursor-pointer">Features</a>
<a href="#courses" class="block px-3 py-2 text-secondary font-medium hover:bg-primary hover:text-white !rounded-button cursor-pointer">Courses</a>
<a href="#community" class="block px-3 py-2 text-secondary font-medium hover:bg-primary hover:text-white !rounded-button cursor-pointer">Community</a>
<a href="#contact" class="block px-3 py-2 text-secondary font-medium hover:bg-primary hover:text-white !rounded-button cursor-pointer">Contact</a>
<a href="#" class="block px-3 py-2 bg-primary text-white font-medium !rounded-button cursor-pointer">Join Now</a>
</div>
</div>
</nav>
<!-- Hero Section -->
<section class="relative overflow-hidden bg-secondary pt-24 pb-16">
<div class="max-w-7xl mx-auto px-4 pt-8 relative z-10">
<div class="text-center md:text-left md:flex md:items-center md:justify-between">
<div class="md:w-1/2">
<h1 class="text-4xl md:text-5xl font-bold text-white leading-tight mb-4">Welcome to <span class="text-primary">Code Club</span></h1>
<p class="text-gray-100 text-lg md:text-xl mb-8 max-w-lg mx-auto md:mx-0">Where coding meets creativity. Join our community of developers and bring your ideas to life.</p>
<div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
<a href="#" class="bg-primary text-white px-8 py-3 !rounded-button font-medium hover:bg-opacity-90 transition-all inline-block cursor-pointer">Get Started</a>
<a href="#courses" class="bg-white text-secondary px-8 py-3 !rounded-button font-medium hover:bg-gray-100 transition-all inline-block cursor-pointer">Explore Courses</a>
</div>
</div>
<div class="md:w-1/2 mt-12 md:mt-0">
<img src="hero.jpg" alt="Coding Environment" class="rounded-lg shadow-2xl mx-auto">
</div>
</div>
</div>
<!-- Floating code snippets -->
<div class="floating-code text-primary text-opacity-20 text-4xl absolute top-20 left-10">&lt;div&gt;</div>
<div class="floating-code text-primary text-opacity-20 text-3xl absolute top-40 right-20">&lt;/&gt;</div>
<div class="floating-code text-primary text-opacity-20 text-5xl absolute bottom-20 left-1/4">{ }</div>
<div class="floating-code text-primary text-opacity-20 text-4xl absolute bottom-40 right-1/4">&lt;/&gt;</div>
</section>
<!-- Stats Section -->
<section class="py-12 bg-white">
<div class="max-w-7xl mx-auto px-4">
<div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
<div class="p-6 bg-gray-50 rounded-lg">
<h3 class="text-3xl font-bold text-secondary mb-2">20+</h3>
<p class="text-gray-600">Active Members</p>
</div>
<div class="p-6 bg-gray-50 rounded-lg">
<h3 class="text-3xl font-bold text-secondary mb-2">40+</h3>
<p class="text-gray-600">Coding Courses</p>
</div>
<div class="p-6 bg-gray-50 rounded-lg">
<h3 class="text-3xl font-bold text-secondary mb-2">98%</h3>
<p class="text-gray-600">Success Rate</p>
</div>
<div class="p-6 bg-gray-50 rounded-lg">
<h3 class="text-3xl font-bold text-secondary mb-2">24/7</h3>
<p class="text-gray-600">Community Support</p>
</div>
</div>
</div>
</section>
<!-- Features Section -->
<section id="features" class="py-16 bg-gray-50">
<div class="max-w-7xl mx-auto px-4">
<div class="text-center mb-16">
<h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">Why Choose Code Club?</h2>
<p class="text-gray-600 max-w-2xl mx-auto">We provide the tools, resources, and community support to help you master coding skills and advance your career.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-code-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Expert-Led Courses</h3>
<p class="text-gray-600">Learn from industry professionals with years of experience in software development and programming.</p>
</div>
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-group-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Supportive Community</h3>
<p class="text-gray-600">Connect with like-minded individuals, collaborate on projects, and grow together as developers.</p>
</div>
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-rocket-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Career Advancement</h3>
<p class="text-gray-600">Gain the skills and portfolio needed to land your dream job or advance in your current role.</p>
</div>
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-tools-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Hands-On Projects</h3>
<p class="text-gray-600">Build real-world applications and strengthen your portfolio with guided project-based learning.</p>
</div>
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-24-hours-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Flexible Learning</h3>
<p class="text-gray-600">Learn at your own pace with on-demand video lessons, exercises, and resources available 24/7.</p>
</div>
<div class="feature-card bg-white p-6 rounded-lg border border-gray-200">
<div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mb-6">
<i class="ri-medal-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-secondary mb-3">Certification</h3>
<p class="text-gray-600">Earn industry-recognized certificates to showcase your skills and expertise to employers.</p>
</div>
</div>
</div>
</section>
<!-- Courses Section -->
<section id="courses" class="py-16 bg-white">
<div class="max-w-7xl mx-auto px-4">
<div class="text-center mb-16">
<h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">Popular Courses</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Explore our most sought-after courses designed to help you master in-demand programming skills.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
<div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-shadow">
<img src="full.jpg" alt="Web Development Course" class="w-full h-48 object-cover">
<div class="p-6">
<div class="flex justify-between items-center mb-3">
<span class="bg-primary bg-opacity-10 text-primary px-3 py-1 rounded-full text-sm font-medium">Beginner</span>
<span class="text-gray-600 text-sm">8 weeks</span>
</div>
<h3 class="text-xl font-semibold text-secondary mb-2">Full-Stack Web Development</h3>
<p class="text-gray-600 mb-4">Master HTML, CSS, JavaScript, React, Node.js, and MongoDB to build complete web applications.</p>
<div class="flex items-center justify-between">
<span class="text-secondary font-bold">$100</span>
<a href="#" class="text-primary font-medium flex items-center cursor-pointer">
View Course <i class="ri-arrow-right-line ml-1"></i>
</a>
</div>
</div>
</div>
<div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-shadow">
<img src="pyth.jpg" alt="Python Course" class="w-full h-48 object-cover">
<div class="p-6">
<div class="flex justify-between items-center mb-3">
<span class="bg-primary bg-opacity-10 text-primary px-3 py-1 rounded-full text-sm font-medium">Intermediate</span>
<span class="text-gray-600 text-sm">10 weeks</span>
</div>
<h3 class="text-xl font-semibold text-secondary mb-2">Python for Data Science</h3>
<p class="text-gray-600 mb-4">Learn Python programming and essential libraries for data analysis, visualization, and machine learning.</p>
<div class="flex items-center justify-between">
<span class="text-secondary font-bold">$200</span>
<a href="#" class="text-primary font-medium flex items-center cursor-pointer">
View Course <i class="ri-arrow-right-line ml-1"></i>
</a>
</div>
</div>
</div>
<div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-shadow">
<img src="mobile.jpg" alt="Mobile Development Course" class="w-full h-48 object-cover">
<div class="p-6">
<div class="flex justify-between items-center mb-3">
<span class="bg-primary bg-opacity-10 text-primary px-3 py-1 rounded-full text-sm font-medium">Advanced</span>
<span class="text-gray-600 text-sm">12 weeks</span>
</div>
<h3 class="text-xl font-semibold text-secondary mb-2">Mobile App Development</h3>
<p class="text-gray-600 mb-4">Build cross-platform mobile applications using React Native for iOS and Android platforms.</p>
<div class="flex items-center justify-between">
<span class="text-secondary font-bold">$299</span>
<a href="#" class="text-primary font-medium flex items-center cursor-pointer">
View Course <i class="ri-arrow-right-line ml-1"></i>
</a>
</div>
</div>
</div>
</div>
<div class="text-center mt-12">
<a href="#" class="bg-secondary text-white px-8 py-3 !rounded-button font-medium hover:bg-opacity-90 transition-all inline-block cursor-pointer">View All Courses</a>
</div>
</div>
</section>
<!-- Testimonials Section -->
<section class="py-16 bg-gray-50">
<div class="max-w-7xl mx-auto px-4">
<div class="text-center mb-16">
<h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">What Our Students Say</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Hear from our community members who have transformed their careers through Code Club.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
<div class="bg-white p-6 rounded-lg shadow-md">
<div class="flex items-center mb-4">
<img src="ino.jpg" alt="Acema Innocent" class="w-12 h-12 rounded-full object-cover mr-4">
<div>
<h4 class="font-semibold text-secondary">Acema Innocent</h4>
<p class="text-sm text-gray-500">Software Engineer at Glasco tech limited</p>
</div>
</div>
<div class="text-yellow-400 mb-3">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
</div>
<p class="text-gray-600">"Code Club completely transformed my career. I went from knowing basic HTML to becoming a full-stack developer in just 6 months. The community support was incredible, and the instructors were always available to help."</p>
</div>
<div class="bg-white p-6 rounded-lg shadow-md">
<div class="flex items-center mb-4">
<img src="jesi.jpg" alt="Mugambwa Augustine" class="w-12 h-12 rounded-full object-cover mr-4">
<div>
<h4 class="font-semibold text-secondary">Mugambwa Augustine</h4>
<p class="text-sm text-gray-500">Frontend Developer at Jessi Corp</p>
</div>
</div>
<div class="text-yellow-400 mb-3">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
</div>
<p class="text-gray-600">"The project-based learning approach at Code Club was exactly what I needed. I built real applications that I could showcase in my portfolio, which ultimately helped me land my dream job at Netflix."</p>
</div>
<div class="bg-white p-6 rounded-lg shadow-md">
<div class="flex items-center mb-4">
<img src="ouma.jpg" alt="Ouma Samuel" class="w-12 h-12 rounded-full object-cover mr-4">
<div>
<h4 class="font-semibold text-secondary">Ouma Samuel</h4>
<p class="text-sm text-gray-500">Data Scientist at Semitech</p>
</div>
</div>
<div class="text-yellow-400 mb-3">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-half-fill"></i>
</div>
<p class="text-gray-600">"As someone transitioning from a non-technical field, I was worried about keeping up. Code Club's structured curriculum and supportive community made learning Python and data science accessible and enjoyable."</p>
</div>
</div>
</div>
</section>
<!-- Community Section -->
<section id="community" class="py-16 bg-white">
<div class="max-w-7xl mx-auto px-4">
<div class="md:flex md:items-center md:justify-between">
<div class="md:w-1/2 mb-10 md:mb-0">
<h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">Join Our Global Community</h2>
<p class="text-gray-600 mb-6">Connect with over 20+ developers worldwide. Share knowledge, collaborate on projects, and grow together.</p>
<ul class="space-y-4 mb-8">
<li class="flex items-start">
<div class="w-6 h-6 flex items-center justify-center mr-3 mt-1">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-gray-600">Weekly coding challenges to sharpen your skills</p>
</li>
<li class="flex items-start">
<div class="w-6 h-6 flex items-center justify-center mr-3 mt-1">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-gray-600">Monthly hackathons with exciting prizes</p>
</li>
<li class="flex items-start">
<div class="w-6 h-6 flex items-center justify-center mr-3 mt-1">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-gray-600">Networking events with industry professionals</p>
</li>
<li class="flex items-start">
<div class="w-6 h-6 flex items-center justify-center mr-3 mt-1">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-gray-600">Job board with exclusive opportunities</p>
</li>
</ul>
<a href="#" class="bg-primary text-white px-8 py-3 !rounded-button font-medium hover:bg-opacity-90 transition-all inline-block cursor-pointer">Join Community</a>
</div>
<div class="md:w-1/2">
<img src="group.jpg" alt="Code Club Community" class="rounded-lg shadow-xl">
</div>
</div>
</div>
</section>
<!-- Newsletter Section -->
<section class="py-16 bg-secondary">
<div class="max-w-7xl mx-auto px-4 text-center">
<h2 class="text-3xl font-bold text-white mb-4">Stay Updated with Code Club</h2>
<p class="text-gray-100 mb-8 max-w-2xl mx-auto">Subscribe to our newsletter for the latest coding tutorials, industry news, and exclusive offers.</p>
<form class="max-w-md mx-auto flex flex-col sm:flex-row gap-4">
<input type="email" placeholder="Enter your email" class="flex-grow px-4 py-3 !rounded-button focus:outline-none focus:ring-2 focus:ring-primary border-none">
<button type="submit" class="bg-primary text-white px-6 py-3 !rounded-button font-medium hover:bg-opacity-90 transition-all cursor-pointer">Subscribe</button>
</form>
</div>
</section>
<!-- Contact Section -->
<section id="contact" class="py-16 bg-white">
<div class="max-w-7xl mx-auto px-4">
<div class="text-center mb-16">
<h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">Get in Touch</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Have questions or need more information? Reach out to our team and we'll get back to you as soon as possible.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-12">
<div>
<form class="space-y-6">
<div>
<label for="name" class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
<input type="text" id="name" class="w-full px-4 py-3 !rounded-button border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
</div>
<div>
<label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
<input type="email" id="email" class="w-full px-4 py-3 !rounded-button border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
</div>
<div>
<label for="subject" class="block text-sm font-medium text-gray-700 mb-1">Subject</label>
<input type="text" id="subject" class="w-full px-4 py-3 !rounded-button border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
</div>
<div>
<label for="message" class="block text-sm font-medium text-gray-700 mb-1">Message</label>
<textarea id="message" rows="5" class="w-full px-4 py-3 !rounded-button border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"></textarea>
</div>
<button type="submit" class="w-full bg-primary text-white px-6 py-3 !rounded-button font-medium hover:bg-opacity-90 transition-all cursor-pointer">Send Message</button>
</form>
</div>
<div>
<div class="bg-gray-50 p-8 rounded-lg h-full">
<h3 class="text-xl font-semibold text-secondary mb-6">Contact Information</h3>
<div class="space-y-6">
<div class="flex items-start">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full mr-4">
<i class="ri-map-pin-line text-primary"></i>
</div>
<div>
<h4 class="font-medium text-secondary mb-1">Location</h4>
<p class="text-gray-600">Uganda, Kampala, keybando, kyebendo kisalosalo</p>
</div>
</div>
<div class="flex items-start">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full mr-4">
<i class="ri-mail-line text-primary"></i>
</div>
<div>
<h4 class="font-medium text-secondary mb-1">Email</h4>
<p class="text-gray-600">info@codeclub.com</p>
</div>
</div>
<div class="flex items-start">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full mr-4">
<i class="ri-phone-line text-primary"></i>
</div>
<div>
<h4 class="font-medium text-secondary mb-1">Phone</h4>
<p class="text-gray-600">+(256) 785801062</p>
</div>
</div>
<div class="flex items-start">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full mr-4">
<i class="ri-time-line text-primary"></i>
</div>
<div>
<h4 class="font-medium text-secondary mb-1">Working Hours</h4>
<p class="text-gray-600">Monday - Friday: 9:00 AM - 6:00 PM</p>
</div>
</div>
</div>
<div class="mt-8">
<h4 class="font-medium text-secondary mb-4">Follow Us</h4>
<div class="flex space-x-4">
<a href="#" class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full hover:bg-primary hover:text-white transition-all cursor-pointer">
<i class="ri-facebook-fill"></i>
</a>
<a href="#" class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full hover:bg-primary hover:text-white transition-all cursor-pointer">
<i class="ri-twitter-fill"></i>
</a>
<a href="#" class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full hover:bg-primary hover:text-white transition-all cursor-pointer">
<i class="ri-linkedin-fill"></i>
</a>
<a href="#" class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full hover:bg-primary hover:text-white transition-all cursor-pointer">
<i class="ri-github-fill"></i>
</a>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- Footer -->
<footer class="bg-secondary text-white py-12">
<div class="max-w-7xl mx-auto px-4">
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
<div>
<a href="#" class="flex items-center mb-4">
<img src="CODE.png" style="width:90px; height:90px;" alt="Code Club Logo" class="h-10">
</a>
<p class="text-gray-300 mb-4">Empowering developers to build the future through code.</p>
<div class="flex space-x-4">
<a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">
<i class="ri-facebook-fill"></i>
</a>
<a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">
<i class="ri-twitter-fill"></i>
</a>
<a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">
<i class="ri-linkedin-fill"></i>
</a>
<a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">
<i class="ri-github-fill"></i>
</a>
</div>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Quick Links</h4>
<ul class="space-y-2">
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Home</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">About us</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Courses</a></li>
<li><a href="#community" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Community</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Contact</a></li>
</ul>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Resources</h4>
<ul class="space-y-2">
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Blog</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Documentation</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Tutorials</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">FAQs</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Support</a></li>
</ul>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Legal</h4>
<ul class="space-y-2">
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Terms of Service</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Privacy Policy</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Cookie Policy</a></li>
<li><a href="#" class="text-gray-300 hover:text-primary transition-colors cursor-pointer">Refund Policy</a></li>
</ul>
</div>
</div>
<div class="border-t border-gray-700 mt-12 pt-8 text-center">
<p class="text-gray-300">© 2025 Code Club. All rights reserved.</p>
</div>
</div>
</footer>
<!-- Back to Top Button -->
<button id="back-to-top" class="fixed bottom-8 right-8 bg-primary text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg opacity-0 invisible transition-all z-50 cursor-pointer">
<i class="ri-arrow-up-line ri-lg"></i>
</button>
<script id="mobile-menu-script">
document.addEventListener('DOMContentLoaded', function() {
const mobileMenuButton = document.getElementById('mobile-menu-button');
const mobileMenu = document.getElementById('mobile-menu');
mobileMenuButton.addEventListener('click', function() {
mobileMenu.classList.toggle('hidden');
if (mobileMenu.classList.contains('hidden')) {
mobileMenuButton.innerHTML = '<i class="ri-menu-line ri-2x text-secondary"></i>';
} else {
mobileMenuButton.innerHTML = '<i class="ri-close-line ri-2x text-secondary"></i>';
}
});
// Close mobile menu when clicking on a link
const mobileLinks = mobileMenu.querySelectorAll('a');
mobileLinks.forEach(link => {
link.addEventListener('click', function() {
mobileMenu.classList.add('hidden');
mobileMenuButton.innerHTML = '<i class="ri-menu-line ri-2x text-secondary"></i>';
});
});
});
</script>
<script id="scroll-script">
document.addEventListener('DOMContentLoaded', function() {
// Smooth scrolling for anchor links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
anchor.addEventListener('click', function(e) {
e.preventDefault();
if (this.getAttribute('href') === '#') return;
const targetId = this.getAttribute('href');
const targetElement = document.querySelector(targetId);
if (targetElement) {
window.scrollTo({
top: targetElement.offsetTop - 80, // Adjust for fixed header
behavior: 'smooth'
});
}
});
});
// Back to top button
const backToTopButton = document.getElementById('back-to-top');
window.addEventListener('scroll', function() {
if (window.pageYOffset > 300) {
backToTopButton.classList.remove('opacity-0', 'invisible');
backToTopButton.classList.add('opacity-100', 'visible');
} else {
backToTopButton.classList.remove('opacity-100', 'visible');
backToTopButton.classList.add('opacity-0', 'invisible');
}
});
backToTopButton.addEventListener('click', function() {
window.scrollTo({
top: 0,
behavior: 'smooth'
});
});
});
</script>
<script id="form-script">
document.addEventListener('DOMContentLoaded', function() {
const contactForm = document.querySelector('#contact form');
const newsletterForm = document.querySelector('section.py-16.bg-secondary form');
if (contactForm) {
contactForm.addEventListener('submit', function(e) {
e.preventDefault();
// Get form values
const name = document.getElementById('name').value;
const email = document.getElementById('email').value;
const subject = document.getElementById('subject').value;
const message = document.getElementById('message').value;
// Basic validation
if (!name || !email || !subject || !message) {
// Create a notification
const notification = document.createElement('div');
notification.className = 'fixed top-4 right-4 bg-red-500 text-white px-6 py-3 rounded-lg shadow-lg z-50';
notification.textContent = 'Please fill in all fields';
document.body.appendChild(notification);
// Remove notification after 3 seconds
setTimeout(() => {
notification.remove();
}, 3000);
return;
}
// Simulate form submission
const submitButton = contactForm.querySelector('button[type="submit"]');
const originalText = submitButton.textContent;
submitButton.disabled = true;
submitButton.innerHTML = '<i class="ri-loader-4-line animate-spin mr-2"></i> Sending...';
setTimeout(() => {
// Create a success notification
const notification = document.createElement('div');
notification.className = 'fixed top-4 right-4 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg z-50';
notification.textContent = 'Message sent successfully!';
document.body.appendChild(notification);
// Reset form
contactForm.reset();
// Reset button
submitButton.disabled = false;
submitButton.textContent = originalText;
// Remove notification after 3 seconds
setTimeout(() => {
notification.remove();
}, 3000);
}, 1500);
});
}
if (newsletterForm) {
newsletterForm.addEventListener('submit', function(e) {
e.preventDefault();
const emailInput = newsletterForm.querySelector('input[type="email"]');
const email = emailInput.value;
if (!email) {
// Create a notification
const notification = document.createElement('div');
notification.className = 'fixed top-4 right-4 bg-red-500 text-white px-6 py-3 rounded-lg shadow-lg z-50';
notification.textContent = 'Please enter your email';
document.body.appendChild(notification);
// Remove notification after 3 seconds
setTimeout(() => {
notification.remove();
}, 3000);
return;
}
// Simulate form submission
const submitButton = newsletterForm.querySelector('button[type="submit"]');
const originalText = submitButton.textContent;
submitButton.disabled = true;
submitButton.innerHTML = '<i class="ri-loader-4-line animate-spin mr-2"></i> Subscribing...';
setTimeout(() => {
// Create a success notification
const notification = document.createElement('div');
notification.className = 'fixed top-4 right-4 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg z-50';
notification.textContent = 'Thanks for subscribing!';
document.body.appendChild(notification);
// Reset form
newsletterForm.reset();
// Reset button
submitButton.disabled = false;
submitButton.textContent = originalText;
// Remove notification after 3 seconds
setTimeout(() => {
notification.remove();
}, 3000);
}, 1500);
});
}
});
</script>
</body>
</html>
