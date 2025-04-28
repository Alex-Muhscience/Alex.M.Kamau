# Personal Portfolio Website

I'll create a comprehensive personal portfolio website that meets all your requirements. Let's break this down into the key components.

## File Structure

```
portfolio-website/
├── index.html          # Homepage
├── about.html          # About page
├── portfolio.html      # Portfolio page
├── contact.html        # Contact page
├── assets/
│   ├── css/
│   │   └── style.css   # Custom CSS (if needed)
│   ├── js/
│   │   └── main.js     # Main JavaScript file
│   └── images/         # All images
├── README.md           # Project documentation
└── robots.txt          # SEO file
```

## 1. index.html (Homepage)

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Professional portfolio of [Your Name], showcasing skills, projects, and contact information.">
    <meta name="keywords" content="portfolio, web developer, full-stack, designer">
    <title>[Your Name] | Full-Stack Developer</title>
    
    <!-- Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="assets/images/favicon.png">
    
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .hero-gradient {
            background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/80 dark:bg-gray-900/80 backdrop-blur-md z-50 shadow-sm">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="index.html" class="text-xl font-bold text-blue-600 dark:text-blue-400">[Your Name]</a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                    <a href="about.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                    <a href="portfolio.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                    <a href="contact.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                    <button id="theme-toggle" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg id="theme-toggle-dark-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"></path>
                        </svg>
                        <svg id="theme-toggle-light-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd" clip-rule="evenodd"></path>
                        </svg>
                    </button>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-button" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-gray-900 shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="index.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                <a href="about.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                <a href="portfolio.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                <a href="contact.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                <button id="mobile-theme-toggle" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">
                    Toggle Dark Mode
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-gradient min-h-screen flex items-center justify-center pt-16">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-20 text-center">
            <div class="flex flex-col md:flex-row items-center justify-between">
                <div class="md:w-1/2 text-left">
                    <h1 class="text-4xl md:text-6xl font-bold text-white mb-4">Hi, I'm <span class="text-blue-200">[Your Name]</span></h1>
                    <h2 class="text-2xl md:text-3xl font-semibold text-blue-100 mb-6">Full-Stack Developer</h2>
                    <p class="text-lg text-blue-50 mb-8 max-w-lg">Crafting user-centric web solutions that drive results and enhance experiences.</p>
                    <div class="flex space-x-4">
                        <a href="portfolio.html" class="bg-white text-blue-600 hover:bg-blue-50 px-6 py-3 rounded-lg font-medium transition duration-300">View Projects</a>
                        <a href="contact.html" class="border-2 border-white text-white hover:bg-white/10 px-6 py-3 rounded-lg font-medium transition duration-300">Contact Me</a>
                    </div>
                </div>
                <div class="md:w-1/2 mt-10 md:mt-0 flex justify-center">
                    <div class="relative">
                        <div class="w-64 h-64 md:w-80 md:h-80 rounded-full bg-blue-200 overflow-hidden border-4 border-white shadow-xl">
                            <!-- Placeholder for headshot - replace with your image -->
                            <img src="https://images.unsplash.com/photo-1531123897727-8f129e1688ce?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&h=400&q=80" 
                                 alt="[Your Name] Headshot" 
                                 class="w-full h-full object-cover"
                                 loading="lazy">
                        </div>
                        <div class="absolute -bottom-5 -right-5 bg-blue-600 text-white px-4 py-2 rounded-lg shadow-lg">
                            <span class="font-bold">5+</span> Years Experience
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">My Skills</h2>
                <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">I've worked with a variety of technologies in the web development world.</p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-8">
                <!-- Skill 1 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">HTML5</h3>
                </div>
                
                <!-- Skill 2 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">CSS3</h3>
                </div>
                
                <!-- Skill 3 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">JavaScript</h3>
                </div>
                
                <!-- Skill 4 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">React</h3>
                </div>
                
                <!-- Skill 5 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">Node.js</h3>
                </div>
                
                <!-- Skill 6 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl text-center hover:shadow-lg transition duration-300">
                    <div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-blue-100 dark:bg-blue-900/30 rounded-lg">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg" alt="Tailwind CSS" class="w-10 h-10" loading="lazy">
                    </div>
                    <h3 class="font-semibold text-lg text-gray-900 dark:text-white">Tailwind CSS</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Projects Section -->
    <section class="py-20 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">Featured Projects</h2>
                <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">Here are some of my recent projects that I'm proud of.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Project 1 -->
                <div class="bg-white dark:bg-gray-900 rounded-xl overflow-hidden shadow-md project-card transition duration-300">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Project 1" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">E-Commerce Platform</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">A full-featured online store with product listings, cart functionality, and secure checkout.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">React</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Node.js</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">MongoDB</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">Live Demo</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="bg-white dark:bg-gray-900 rounded-xl overflow-hidden shadow-md project-card transition duration-300">
                    <img src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Project 2" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Task Management App</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">A productivity application for organizing tasks with drag-and-drop functionality and team collaboration.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Vue.js</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Tailwind CSS</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">Live Demo</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="portfolio.html" class="inline-block bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-medium transition duration-300">View All Projects</a>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">What People Say</h2>
                <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">Feedback from clients and colleagues I've worked with.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Sarah Johnson" class="w-full h-full object-cover" loading="lazy">
                        </div>
                        <div>
                            <h4 class="font-bold text-gray-900 dark:text-white">Sarah Johnson</h4>
                            <p class="text-gray-600 dark:text-gray-400 text-sm">CEO, TechStart</p>
                        </div>
                    </div>
                    <p class="text-gray-700 dark:text-gray-300 italic">"Working with [Your Name] was an absolute pleasure. Their attention to detail and problem-solving skills helped us launch our platform ahead of schedule."</p>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Michael Chen" class="w-full h-full object-cover" loading="lazy">
                        </div>
                        <div>
                            <h4 class="font-bold text-gray-900 dark:text-white">Michael Chen</h4>
                            <p class="text-gray-600 dark:text-gray-400 text-sm">Product Manager, InnovateCo</p>
                        </div>
                    </div>
                    <p class="text-gray-700 dark:text-gray-300 italic">"[Your Name] delivered exceptional results on our complex web application. Their technical expertise and communication were outstanding throughout the project."</p>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Emily Rodriguez" class="w-full h-full object-cover" loading="lazy">
                        </div>
                        <div>
                            <h4 class="font-bold text-gray-900 dark:text-white">Emily Rodriguez</h4>
                            <p class="text-gray-600 dark:text-gray-400 text-sm">Design Lead, CreativeMinds</p>
                        </div>
                    </div>
                    <p class="text-gray-700 dark:text-gray-300 italic">"Collaborating with [Your Name] was seamless. They understood our design vision perfectly and implemented it with precision and creativity."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 hero-gradient">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Ready to start your project?</h2>
            <p class="text-xl text-blue-100 mb-8 max-w-2xl mx-auto">I'm currently available for freelance work or full-time positions. Let's build something amazing together!</p>
            <a href="contact.html" class="inline-block bg-white text-blue-600 hover:bg-blue-50 px-8 py-4 rounded-lg font-bold text-lg transition duration-300">Get In Touch</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <h3 class="text-xl font-bold text-white mb-4">[Your Name]</h3>
                    <p class="mb-4">Full-stack developer passionate about creating beautiful, functional web experiences.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="hover:text-white transition duration-300">Home</a></li>
                        <li><a href="about.html" class="hover:text-white transition duration-300">About</a></li>
                        <li><a href="portfolio.html" class="hover:text-white transition duration-300">Portfolio</a></li>
                        <li><a href="contact.html" class="hover:text-white transition duration-300">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Contact Info</h4>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                            </svg>
                            <span>your.email@example.com</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                            </svg>
                            <span>+1 (555) 123-4567</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                            <span>San Francisco, CA</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 [Your Name]. All rights reserved.</p>
                <a href="#" class="mt-4 md:mt-0 inline-flex items-center text-blue-400 hover:text-blue-300">
                    Back to Top
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18"></path>
                    </svg>
                </a>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script src="assets/js/main.js"></script>
</body>
</html>
```

## 2. about.html

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Learn more about [Your Name], a Full-Stack Developer with expertise in web technologies.">
    <meta name="keywords" content="about, bio, resume, skills, experience">
    <title>About | [Your Name]</title>
    
    <!-- Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="assets/images/favicon.png">
    
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .timeline-item:not(:last-child):after {
            content: '';
            position: absolute;
            left: 7px;
            top: 24px;
            height: 100%;
            width: 2px;
            background: #e5e7eb;
        }
        .dark .timeline-item:not(:last-child):after {
            background: #374151;
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/80 dark:bg-gray-900/80 backdrop-blur-md z-50 shadow-sm">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="index.html" class="text-xl font-bold text-blue-600 dark:text-blue-400">[Your Name]</a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                    <a href="about.html" class="text-blue-600 dark:text-blue-400 font-medium">About</a>
                    <a href="portfolio.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                    <a href="contact.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                    <button id="theme-toggle" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg id="theme-toggle-dark-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"></path>
                        </svg>
                        <svg id="theme-toggle-light-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd" clip-rule="evenodd"></path>
                        </svg>
                    </button>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-button" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-gray-900 shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="index.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                <a href="about.html" class="block px-3 py-2 rounded-md text-base font-medium text-blue-600 dark:text-blue-400">About</a>
                <a href="portfolio.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                <a href="contact.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                <button id="mobile-theme-toggle" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">
                    Toggle Dark Mode
                </button>
            </div>
        </div>
    </nav>

    <!-- About Hero Section -->
    <section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-12">
                <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">About Me</h1>
                <p class="text-xl text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">Get to know the person behind the code.</p>
            </div>
            
            <div class="flex flex-col md:flex-row items-center justify-between gap-12">
                <div class="md:w-1/2">
                    <div class="relative">
                        <div class="w-full h-96 md:h-auto rounded-2xl overflow-hidden shadow-xl">
                            <!-- Placeholder for about image - replace with your image -->
                            <img src="https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=600&q=80" 
                                 alt="[Your Name] working" 
                                 class="w-full h-full object-cover"
                                 loading="lazy">
                        </div>
                        <div class="absolute -bottom-5 -left-5 bg-blue-600 text-white px-6 py-3 rounded-lg shadow-lg">
                            <span class="font-bold">100%</span> Dedicated
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-900 dark:text-white mb-6">Who Am I?</h2>
                    <div class="prose dark:prose-invert max-w-none">
                        <p class="mb-4">I'm a passionate full-stack developer with over 5 years of experience building web applications that solve real-world problems. My journey in tech began when I built my first website at 15, and I've been hooked ever since.</p>
                        <p class="mb-4">I specialize in JavaScript technologies across the stack, with expertise in React, Node.js, and modern CSS frameworks like Tailwind. What drives me is creating intuitive, accessible digital experiences that make people's lives easier.</p>
                        <p class="mb-6">When I'm not coding, you can find me hiking in the mountains, experimenting with new coffee brewing methods, or contributing to open-source projects.</p>
                        
                        <div class="flex flex-wrap gap-4">
                            <a href="#experience" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-medium transition duration-300">My Experience</a>
                            <a href="assets/documents/resume.pdf" download class="border-2 border-blue-600 text-blue-600 dark:text-blue-400 dark:border-blue-400 hover:bg-blue-50 dark:hover:bg-blue-900/30 px-6 py-3 rounded-lg font-medium transition duration-300">Download Resume</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Bio Section -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-4">My Story</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto"></div>
            </div>
            
            <div class="prose dark:prose-invert max-w-none">
                <p class="mb-4">Growing up, I was always fascinated by how things worked. I would take apart gadgets just to put them back together (sometimes successfully). This curiosity naturally led me to programming, where I discovered the joy of building things from scratch.</p>
                
                <p class="mb-4">After earning my Computer Science degree from [Your University], I began my professional career at [First Company], where I cut my teeth on enterprise web applications. There, I learned the importance of writing clean, maintainable code and collaborating effectively with teams.</p>
                
                <p class="mb-4">My career has taken me through startups and established companies, each teaching me valuable lessons about scalability, user experience, and the business impact of technology. I've had the privilege of mentoring junior developers and leading projects that serve millions of users.</p>
                
                <p class="mb-4">What excites me most about web development is how rapidly the ecosystem evolves. I make it a priority to stay current with emerging technologies while maintaining a solid foundation in core web principles. This balance allows me to adopt new tools judiciously and avoid chasing every new trend.</p>
                
                <p class="mb-4">Beyond technical skills, I believe great developers are defined by their ability to communicate complex ideas clearly, empathize with users, and approach problems creatively. These are the qualities I continue to cultivate in myself and appreciate in others.</p>
                
                <div class="bg-blue-50 dark:bg-blue-900/20 p-6 rounded-xl my-8 border-l-4 border-blue-600">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Fun Fact</h3>
                    <p class="text-gray-700 dark:text-gray-300">I'm a certified coffee enthusiast and can tell you the difference between a Chemex and AeroPress brew. My current favorite is a light roast Ethiopian with floral notes.</p>
                </div>
                
                <p>When I'm not at my desk, you'll find me outdoors hiking or cycling, at a local coffee shop with a book, or volunteering with organizations that teach coding to underrepresented groups in tech. I'm always looking for new challenges and opportunities to grow both as a developer and as a person.</p>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-20 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-4">Experience & Education</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto"></div>
            </div>
            
            <div class="space-y-8">
                <!-- Experience 1 -->
                <div class="timeline-item relative pl-8">
                    <div class="absolute left-0 top-0 w-4 h-4 rounded-full bg-blue-600 border-4 border-white dark:border-gray-800 z-10"></div>
                    <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-md">
                        <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-2">
                            <h3 class="text-xl font-bold text-gray-900 dark:text-white">Senior Full-Stack Developer</h3>
                            <span class="text-blue-600 dark:text-blue-400 font-medium">2021 - Present</span>
                        </div>
                        <h4 class="text-lg text-gray-700 dark:text-gray-300 mb-4">TechSolutions Inc.</h4>
                        <p class="text-gray-600 dark:text-gray-400">Led a team of 5 developers in building a SaaS platform serving 10,000+ users. Architected the frontend using React with TypeScript and the backend with Node.js and PostgreSQL. Implemented CI/CD pipelines reducing deployment time by 40%.</p>
                    </div>
                </div>
                
                <!-- Experience 2 -->
                <div class="timeline-item relative pl-8">
                    <div class="absolute left-0 top-0 w-4 h-4 rounded-full bg-blue-600 border-4 border-white dark:border-gray-800 z-10"></div>
                    <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-md">
                        <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-2">
                            <h3 class="text-xl font-bold text-gray-900 dark:text-white">Frontend Developer</h3>
                            <span class="text-blue-600 dark:text-blue-400 font-medium">2018 - 2021</span>
                        </div>
                        <h4 class="text-lg text-gray-700 dark:text-gray-300 mb-4">Digital Innovations LLC</h4>
                        <p class="text-gray-600 dark:text-gray-400">Developed responsive web applications using React and Redux. Collaborated with designers to implement pixel-perfect UIs. Improved application performance by 30% through code optimization and lazy loading techniques.</p>
                    </div>
                </div>
                
                <!-- Education 1 -->
                <div class="timeline-item relative pl-8">
                    <div class="absolute left-0 top-0 w-4 h-4 rounded-full bg-blue-600 border-4 border-white dark:border-gray-800 z-10"></div>
                    <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-md">
                        <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-2">
                            <h3 class="text-xl font-bold text-gray-900 dark:text-white">B.S. Computer Science</h3>
                            <span class="text-blue-600 dark:text-blue-400 font-medium">2014 - 2018</span>
                        </div>
                        <h4 class="text-lg text-gray-700 dark:text-gray-300 mb-4">State University</h4>
                        <p class="text-gray-600 dark:text-gray-400">Graduated with honors. Specialized in Web Technologies and Human-Computer Interaction. Served as president of the Computer Science Club and organized hackathons with 200+ participants.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-4">Technical Skills</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Frontend Skills -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl">
                    <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-4 flex items-center">
                        <svg class="w-6 h-6 mr-2 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                        </svg>
                        Frontend Development
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">HTML/CSS</span>
                                <span class="text-gray-500 dark:text-gray-400">Expert</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">JavaScript</span>
                                <span class="text-gray-500 dark:text-gray-400">Expert</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">React</span>
                                <span class="text-gray-500 dark:text-gray-400">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">Tailwind CSS</span>
                                <span class="text-gray-500 dark:text-gray-400">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Backend Skills -->
                <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-xl">
                    <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-4 flex items-center">
                        <svg class="w-6 h-6 mr-2 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01"></path>
                        </svg>
                        Backend Development
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">Node.js</span>
                                <span class="text-gray-500 dark:text-gray-400">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">Express</span>
                                <span class="text-gray-500 dark:text-gray-400">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">MongoDB</span>
                                <span class="text-gray-500 dark:text-gray-400">Intermediate</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 75%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="text-gray-700 dark:text-gray-300">PostgreSQL</span>
                                <span class="text-gray-500 dark:text-gray-400">Intermediate</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 70%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 bg-blue-600 text-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">Want to work together?</h2>
            <p class="text-lg text-blue-100 mb-8 max-w-2xl mx-auto">I'm always interested in hearing about new projects and opportunities. Let's connect!</p>
            <a href="contact.html" class="inline-block bg-white text-blue-600 hover:bg-blue-50 px-8 py-3 rounded-lg font-bold text-lg transition duration-300">Contact Me</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <h3 class="text-xl font-bold text-white mb-4">[Your Name]</h3>
                    <p class="mb-4">Full-stack developer passionate about creating beautiful, functional web experiences.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="hover:text-white transition duration-300">Home</a></li>
                        <li><a href="about.html" class="hover:text-white transition duration-300">About</a></li>
                        <li><a href="portfolio.html" class="hover:text-white transition duration-300">Portfolio</a></li>
                        <li><a href="contact.html" class="hover:text-white transition duration-300">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Contact Info</h4>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                            </svg>
                            <span>your.email@example.com</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                            </svg>
                            <span>+1 (555) 123-4567</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                            <span>San Francisco, CA</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 [Your Name]. All rights reserved.</p>
                <a href="#" class="mt-4 md:mt-0 inline-flex items-center text-blue-400 hover:text-blue-300">
                    Back to Top
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18"></path>
                    </svg>
                </a>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script src="assets/js/main.js"></script>
</body>
</html>
```

## 3. portfolio.html

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfolio of projects by [Your Name], showcasing web development work and case studies.">
    <meta name="keywords" content="portfolio, projects, web development, case studies">
    <title>Portfolio | [Your Name]</title>
    
    <!-- Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="assets/images/favicon.png">
    
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .project-card {
            transition: all 0.3s ease;
        }
        .project-card:hover {
            transform: translateY(-5px);
        }
        .filter-btn.active {
            background-color: #3b82f6;
            color: white;
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/80 dark:bg-gray-900/80 backdrop-blur-md z-50 shadow-sm">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="index.html" class="text-xl font-bold text-blue-600 dark:text-blue-400">[Your Name]</a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                    <a href="about.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                    <a href="portfolio.html" class="text-blue-600 dark:text-blue-400 font-medium">Portfolio</a>
                    <a href="contact.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                    <button id="theme-toggle" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg id="theme-toggle-dark-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"></path>
                        </svg>
                        <svg id="theme-toggle-light-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd" clip-rule="evenodd"></path>
                        </svg>
                    </button>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-button" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-gray-900 shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="index.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                <a href="about.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                <a href="portfolio.html" class="block px-3 py-2 rounded-md text-base font-medium text-blue-600 dark:text-blue-400">Portfolio</a>
                <a href="contact.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Contact</a>
                <button id="mobile-theme-toggle" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">
                    Toggle Dark Mode
                </button>
            </div>
        </div>
    </nav>

    <!-- Portfolio Hero Section -->
    <section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto text-center">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">My Portfolio</h1>
            <p class="text-xl text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">A collection of my recent projects and case studies.</p>
        </div>
    </section>

    <!-- Portfolio Filter -->
    <section class="py-8 bg-white dark:bg-gray-900 sticky top-16 z-40 shadow-sm">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-wrap justify-center gap-4">
                <button class="filter-btn px-4 py-2 rounded-full bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition duration-300 active" data-filter="all">All</button>
                <button class="filter-btn px-4 py-2 rounded-full bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition duration-300" data-filter="web">Web Development</button>
                <button class="filter-btn px-4 py-2 rounded-full bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition duration-300" data-filter="mobile">Mobile</button>
                <button class="filter-btn px-4 py-2 rounded-full bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition duration-300" data-filter="design">Design</button>
            </div>
        </div>
    </section>

    <!-- Projects Grid -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="web">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="E-Commerce Platform" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">E-Commerce Platform</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">A full-featured online store with product listings, cart functionality, and secure checkout.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">React</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Node.js</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">MongoDB</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">Live Demo</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="web">
                    <img src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Task Management App" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Task Management App</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">A productivity application for organizing tasks with drag-and-drop functionality and team collaboration.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Vue.js</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Tailwind CSS</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">Live Demo</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="mobile">
                    <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Fitness Tracker App" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Fitness Tracker App</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">Mobile application for tracking workouts, nutrition, and progress with personalized recommendations.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">React Native</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Redux</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">App Store</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 4 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="design">
                    <img src="https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Brand Identity Design" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Brand Identity Design</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">Complete brand identity package including logo, color palette, typography, and brand guidelines.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Illustrator</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Photoshop</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Figma</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">View Case Study</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">Behance</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 5 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="web">
                    <img src="https://images.unsplash.com/photo-1522542550221-31fd19575a2d?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Real Estate Platform" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Real Estate Platform</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">A comprehensive platform for property listings with advanced search filters and virtual tours.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Next.js</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Strapi</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">PostgreSQL</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">Live Demo</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 6 -->
                <div class="project-card bg-gray-50 dark:bg-gray-800 rounded-xl overflow-hidden shadow-md" data-category="mobile">
                    <img src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=300&q=80" 
                         alt="Food Delivery App" 
                         class="w-full h-48 object-cover"
                         loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Food Delivery App</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">Mobile application for ordering food from local restaurants with real-time tracking.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Flutter</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-200 px-3 py-1 rounded-full text-sm">Google Maps API</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-600 dark:text-blue-400 hover:underline font-medium">App Store</a>
                            <a href="#" class="text-gray-600 dark:text-gray-400 hover:underline font-medium">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 bg-blue-600 text-white">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">Have a project in mind?</h2>
            <p class="text-lg text-blue-100 mb-8 max-w-2xl mx-auto">I'm always excited to hear about new opportunities and challenges.</p>
            <a href="contact.html" class="inline-block bg-white text-blue-600 hover:bg-blue-50 px-8 py-3 rounded-lg font-bold text-lg transition duration-300">Let's Talk</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <h3 class="text-xl font-bold text-white mb-4">[Your Name]</h3>
                    <p class="mb-4">Full-stack developer passionate about creating beautiful, functional web experiences.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.505.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="hover:text-white transition duration-300">Home</a></li>
                        <li><a href="about.html" class="hover:text-white transition duration-300">About</a></li>
                        <li><a href="portfolio.html" class="hover:text-white transition duration-300">Portfolio</a></li>
                        <li><a href="contact.html" class="hover:text-white transition duration-300">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Contact Info</h4>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                            </svg>
                            <span>your.email@example.com</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                            </svg>
                            <span>+1 (555) 123-4567</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                            <span>San Francisco, CA</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 [Your Name]. All rights reserved.</p>
                <a href="#" class="mt-4 md:mt-0 inline-flex items-center text-blue-400 hover:text-blue-300">
                    Back to Top
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18"></path>
                    </svg>
                </a>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script src="assets/js/main.js"></script>
    <script>
        // Portfolio filtering
        document.addEventListener('DOMContentLoaded', function() {
            const filterButtons = document.querySelectorAll('.filter-btn');
            const projectCards = document.querySelectorAll('.project-card');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Remove active class from all buttons
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    // Add active class to clicked button
                    this.classList.add('active');
                    
                    const filterValue = this.getAttribute('data-filter');
                    
                    projectCards.forEach(card => {
                        if (filterValue === 'all' || card.getAttribute('data-category') === filterValue) {
                            card.style.display = 'block';
                        } else {
                            card.style.display = 'none';
                        }
                    });
                });
            });
        });
    </script>
</body>
</html>
```

## 4. contact.html

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Contact [Your Name], a Full-Stack Developer, for project inquiries and collaborations.">
    <meta name="keywords" content="contact, hire, web developer, full-stack, collaboration">
    <title>Contact | [Your Name]</title>
    
    <!-- Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="assets/images/favicon.png">
    
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .input-error {
            border-color: #ef4444;
        }
        .error-message {
            color: #ef4444;
            font-size: 0.875rem;
            margin-top: 0.25rem;
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/80 dark:bg-gray-900/80 backdrop-blur-md z-50 shadow-sm">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="index.html" class="text-xl font-bold text-blue-600 dark:text-blue-400">[Your Name]</a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                    <a href="about.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                    <a href="portfolio.html" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                    <a href="contact.html" class="text-blue-600 dark:text-blue-400 font-medium">Contact</a>
                    <button id="theme-toggle" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg id="theme-toggle-dark-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"></path>
                        </svg>
                        <svg id="theme-toggle-light-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd" clip-rule="evenodd"></path>
                        </svg>
                    </button>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-button" class="p-2 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-gray-900 shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="index.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Home</a>
                <a href="about.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">About</a>
                <a href="portfolio.html" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">Portfolio</a>
                <a href="contact.html" class="block px-3 py-2 rounded-md text-base font-medium text-blue-600 dark:text-blue-400">Contact</a>
                <button id="mobile-theme-toggle" class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">
                    Toggle Dark Mode
                </button>
            </div>
        </div>
    </nav>

    <!-- Contact Hero Section -->
    <section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto text-center">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">Get In Touch</h1>
            <p class="text-xl text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">Have a project in mind or want to collaborate? I'd love to hear from you.</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="py-20 bg-white dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div>
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-900 dark:text-white mb-6">Send Me a Message</h2>
                    <p class="text-gray-600 dark:text-gray-300 mb-8">Fill out the form below and I'll get back to you as soon as possible. Typically within 24 hours.</p>
                    
                    <form id="contact-form" class="space-y-6" action="https://formspree.io/f/your-form-id" method="POST">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Name</label>
                            <input type="text" id="name" name="name" class="w-full px-4 py-3 rounded-lg border border-gray-300 dark:border-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-800 dark:text-white transition duration-300" required>
                            <div id="name-error" class="error-message hidden">Please enter your name</div>
                        </div>
                        
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Email</label>
                            <input type="email" id="email" name="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 dark:border-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-800 dark:text-white transition duration-300" required>
                            <div id="email-error" class="error-message hidden">Please enter a valid email address</div>
                        </div>
                        
                        <div>
                            <label for="subject" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Subject</label>
                            <input type="text" id="subject" name="subject" class="w-full px-4 py-3 rounded-lg border border-gray-300 dark:border-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-800 dark:text-white transition duration-300" required>
                            <div id="subject-error" class="error-message hidden">Please enter a subject</div>
                        </div>
                        
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Message</label>
                            <textarea id="message" name="message" rows="5" class="w-full px-4 py-3 rounded-lg border border-gray-300 dark:border-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-800 dark:text-white transition duration-300" required></textarea>
                            <div id="message-error" class="error-message hidden">Please enter your message</div>
                        </div>
                        
                        <div>
                            <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-medium w-full transition duration-300">Send Message</button>
                        </div>
                        
                        <div id="form-success" class="hidden p-4 mb-4 text-sm text-green-700 bg-green-100 rounded-lg dark:bg-green-200 dark:text-green-800">
                            Thank you! Your message has been sent successfully. I'll get back to you soon.
                        </div>
                        
                        <div id="form-error" class="hidden p-4 mb-4 text-sm text-red-700 bg-red-100 rounded-lg dark:bg-red-200 dark:text-red-800">
                            There was an error submitting your message. Please try again later.
                        </div>
                    </form>
                </div>
                
                <div>
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-900 dark:text-white mb-6">Contact Information</h2>
                    <p class="text-gray-600 dark:text-gray-300 mb-8">Prefer to reach out directly? Here's how you can get in touch with me.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="flex-shrink-0 bg-blue-100 dark:bg-blue-900/30 p-3 rounded-lg">
                                <svg class="w-6 h-6 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                </svg>
                            </div>
                            <div class="ml-4">
                                <h3 class="text-lg font-medium text-gray-900 dark:text-white">Email</h3>
                                <p class="text-gray-600 dark:text-gray-400 mt-1">your.email@example.com</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="flex-shrink-0 bg-blue-100 dark:bg-blue-900/30 p-3 rounded-lg">
                                <svg class="w-6 h-6 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                                </svg>
                            </div>
                            <div class="ml-4">
                                <h3 class="text-lg font-medium text-gray-900 dark:text-white">Phone</h3>
                                <p class="text-gray-600 dark:text-gray-400 mt-1">+1 (555) 123-4567</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="flex-shrink-0 bg-blue-100 dark:bg-blue-900/30 p-3 rounded-lg">
                                <svg class="w-6 h-6 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                </svg>
                            </div>
                            <div class="ml-4">
                                <h3 class="text-lg font-medium text-gray-900 dark:text-white">Location</h3>
                                <p class="text-gray-600 dark:text-gray-400 mt-1">San Francisco, CA</p>
                            </div>
                        </div>
                        
                        <div class="pt-6">
                            <h3 class="text-lg font-medium text-gray-900 dark:text-white mb-4">Connect With Me</h3>
                            <div class="flex space-x-4">
                                <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-blue-600 dark:hover:text-blue-400 transition duration-300">
                                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                        <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"></path>
                                    </svg>
                                </a>
                                <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-blue-600 dark:hover:text-blue-400 transition duration-300">
                                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                        <path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.505.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path>
                                    </svg>
                                </a>
                                <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-blue-600 dark:hover:text-blue-400 transition duration-300">
                                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                        <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                                    </svg>
                                </a>
                                <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-blue-600 dark:hover:text-blue-400 transition duration-300">
                                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                        <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"></path>
                                    </svg>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <section class="bg-gray-100 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3153.538443441068!2d-122.4194156846823!3d37.77492997975921!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80859a6d00690021%3A0x4a501367f076adff!2sSan%20Francisco%2C%20CA!5e0!3m2!1sen!2sus!4v1620000000000!5m2!1sen!2sus" 
                    width="100%" 
                    height="400" 
                    style="border:0;" 
                    allowfullscreen="" 
                    loading="lazy"
                    class="dark:grayscale dark:opacity-70"></iframe>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <h3 class="text-xl font-bold text-white mb-4">[Your Name]</h3>
                    <p class="mb-4">Full-stack developer passionate about creating beautiful, functional web experiences.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.505.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition duration-300">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"></path>
                            </svg>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="hover:text-white transition duration-300">Home</a></li>
                        <li><a href="about.html" class="hover:text-white transition duration-300">About</a></li>
                        <li><a href="portfolio.html" class="hover:text-white transition duration-300">Portfolio</a></li>
                        <li><a href="contact.html" class="hover:text-white transition duration-300">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold text-white mb-4">Contact Info</h4>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                            </svg>
                            <span>your.email@example.com</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                            </svg>
                            <span>+1 (555) 123-4567</span>
                        </li>
                        <li class="flex items-start">
                            <svg class="w-5 h-5 mr-2 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                            <span>San Francisco, CA</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 [Your Name]. All rights reserved.</p>
                <a href="#" class="mt-4 md:mt-0 inline-flex items-center text-blue-400 hover:text-blue-300">
                    Back to Top
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18"></path>
                    </svg>
                </a>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script src="assets/js/main.js"></script>
    <script>
        // Contact form validation
        document.addEventListener('DOMContentLoaded', function() {
            const contactForm = document.getElementById('contact-form');
            const nameInput = document.getElementById('name');
            const emailInput = document.getElementById('email');
            const subjectInput = document.getElementById('subject');
            const messageInput = document.getElementById('message');
            const nameError = document.getElementById('name-error');
            const emailError = document.getElementById('email-error');
            const subjectError = document.getElementById('subject-error');
            const messageError = document.getElementById('message-error');
            const formSuccess = document.getElementById('form-success');
            const formError = document.getElementById('form-error');
            
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                let isValid = true;
                
                // Reset errors
                nameError.classList.add('hidden');
                emailError.classList.add('hidden');
                subjectError.classList.add('hidden');
                messageError.classList.add('hidden');
                nameInput.classList.remove('input-error');
                emailInput.classList.remove('input-error');
                subjectInput.classList.remove('input-error');
                messageInput.classList.remove('input-error');
                formSuccess.classList.add('hidden');
                formError.classList.add('hidden');
                
                // Validate name
                if (nameInput.value.trim() === '') {
                    nameError.classList.remove('hidden');
                    nameInput.classList.add('input-error');
                    isValid = false;
                }
                
                // Validate email
                const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                if (!emailRegex.test(emailInput.value.trim())) {
                    emailError.classList.remove('hidden');
                    emailInput.classList.add('input-error');
                    isValid = false;
                }
                
                // Validate subject
                if (subjectInput.value.trim() === '') {
                    subjectError.classList.remove('hidden');
                    subjectInput.classList.add('input-error');
                    isValid = false;
                }
                
                // Validate message
                if (messageInput.value.trim() === '') {
                    messageError.classList.remove('hidden');
                    messageInput.classList.add('input-error');
                    isValid = false;
                }
                
                if (isValid) {
                    // Here you would typically send the form data to a server
                    // For demo purposes, we'll just show a success message
                    formSuccess.classList.remove('hidden');
                    contactForm.reset();
                    
                    // In a real implementation, you would use fetch or XMLHttpRequest
                    // to send the form data to your server or Formspree endpoint
                    /*
                    fetch(contactForm.action, {
                        method: 'POST',
                        body: new FormData(contactForm),
                        headers: {
                            'Accept': 'application/json'
                        }
                    })
                    .then(response => {
                        if (response.ok) {
                            formSuccess.classList.remove('hidden');
                            contactForm.reset();
                        } else {
                            formError.classList.remove('hidden');
                        }
                    })
                    .catch(error => {
                        formError.classList.remove('hidden');
                    });
                    */
                }
            });
        });
    </script>
</body>
</html>
```

## 5. assets/js/main.js

```javascript
// Mobile menu toggle
document.addEventListener('DOMContentLoaded', function() {
    const mobileMenuButton = document.getElementById('mobile-menu-button');
    const mobileMenu = document.getElementById('mobile-menu');
    
    if (mobileMenuButton && mobileMenu) {
        mobileMenuButton.addEventListener('click', function() {
            mobileMenu.classList.toggle('hidden');
        });
    }
    
    // Theme toggle functionality
    const themeToggle = document.getElementById('theme-toggle');
    const mobileThemeToggle = document.getElementById('mobile-theme-toggle');
    const themeToggleDarkIcon = document.getElementById('theme-toggle-dark-icon');
    const themeToggleLightIcon = document.getElementById('theme-toggle-light-icon');
    
    // Check for saved user preference or use system preference
    if (localStorage.getItem('color-theme') === 'dark' || (!localStorage.getItem('color-theme') && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
        document.documentElement.classList.add('dark');
        themeToggleLightIcon.classList.remove('hidden');
    } else {
        document.documentElement.classList.remove('dark');
        themeToggleDarkIcon.classList.remove('hidden');
    }
    
    // Toggle theme
    function toggleTheme() {
        // Toggle icons
        themeToggleDarkIcon.classList.toggle('hidden');
        themeToggleLightIcon.classList.toggle('hidden');
        
        // Toggle dark class
        document.documentElement.classList.toggle('dark');
        
        // Save preference to localStorage
        if (document.documentElement.classList.contains('dark')) {
            localStorage.setItem('color-theme', 'dark');
        } else {
            localStorage.setItem('color-theme', 'light');
        }
    }
    
    if (themeToggle) {
        themeToggle.addEventListener('click', toggleTheme);
    }
    
    if (mobileThemeToggle) {
        mobileThemeToggle.addEventListener('click', function() {
            toggleTheme();
            mobileMenu.classList.add('hidden');
        });
    }
    
    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            
            const targetId = this.getAttribute('href');
            if (targetId === '#') return;
            
            const targetElement = document.querySelector(targetId);
            if (targetElement) {
                targetElement.scrollIntoView({
                    behavior: 'smooth'
                });
            }
        });
    });
    
    // Close mobile menu when clicking on a link
    const mobileMenuLinks = document.querySelectorAll('#mobile-menu a');
    mobileMenuLinks.forEach(link => {
        link.addEventListener('click', function() {
            mobileMenu.classList.add('hidden');
        });
    });
});

// Google Analytics (replace with your tracking ID)
/*
window.dataLayer = window.dataLayer || [];
function gtag(){dataLayer.push(arguments);}
gtag('js', new Date());
gtag('config', 'YOUR_GA_TRACKING_ID');
*/
```

## 6. README.md

```markdown
# Personal Portfolio Website

A responsive, modern personal portfolio website built with HTML, CSS, JavaScript, and Tailwind CSS.

## Features

- Responsive design for all device sizes
- Dark/light mode toggle
- Four main pages: Home, About, Portfolio, Contact
- Project filtering on Portfolio page
- Form validation on Contact page
- Smooth scrolling and animations
- SEO optimized with meta tags
- Accessible design following WCAG guidelines

## Technologies Used

- HTML5
- CSS3 (with Tailwind CSS)
- JavaScript
- Tailwind CSS (via CDN)
- Google Fonts (Poppins)
- Formspree for contact form submissions

## Getting Started

### Prerequisites

- Web browser (Chrome, Firefox, Safari, Edge)
- Code editor (VS Code recommended)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/portfolio-website.git
   ```

2. Open the project folder in your code editor.

3. Open `index.html` in your browser to view the website locally.

## Deployment

This website can be deployed to any static hosting service:

### Netlify

1. Drag and drop the project folder to Netlify's drop zone.
2. Follow the prompts to complete deployment.

### Vercel

1. Install Vercel CLI:

   ```bash
   npm install -g vercel
   ```

2. Deploy:

   ```bash
   vercel
   ```

## Customization

To personalize this portfolio:

1. Replace placeholder content in HTML files with your own information.
2. Update images in the `assets/images` folder.
3. Change colors in Tailwind classes to match your brand.
4. Update the Formspree form action URL in `contact.html` with your own Formspree endpoint.

## File Structure

```
portfolio-website/
├── index.html          # Homepage
├── about.html          # About page
├── portfolio.html      # Portfolio page
├── contact.html        # Contact page
├── assets/
│   ├── css/
│   │   └── style.css   # Custom CSS (if needed)
│   ├── js/
│   │   └── main.js     # Main JavaScript file
│   └── images/         # All images
├── README.md           # Project documentation
└── robots.txt          # SEO file
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Tailwind CSS for utility-first styling
- Unsplash for placeholder images
- Formspree for form handling
- Google Fonts for typography

```

## 7. robots.txt

```

User-agent: *
Allow: /

Sitemap: <https://yourdomain.com/sitemap.xml>

```

