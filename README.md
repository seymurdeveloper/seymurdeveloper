<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seymur Yusubov | Developer Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3B82F6',
                        dark: '#1E293B',
                        light: '#F8FAFC'
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'float-reverse': 'float-reverse 5s ease-in-out infinite',
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        'float-reverse': {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(20px)' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom CSS for additional effects */
        .gradient-text {
            background: linear-gradient(90deg, #3B82F6, #8B5CF6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .glass-effect {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .parallax-bg {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
        
        .social-icon:hover {
            transform: translateY(-5px);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            transition: all 0.3s ease;
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #F1F5F9;
        }
        
        ::-webkit-scrollbar-thumb {
            background: #3B82F6;
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: #2563EB;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 font-sans antialiased">
    <!-- Cursor Effect -->
    <div id="cursor" class="fixed w-8 h-8 rounded-full border-2 border-blue-500 pointer-events-none z-50 transform -translate-x-1/2 -translate-y-1/2 mix-blend-difference"></div>
    
    <!-- Loading Screen -->
    <div id="loading" class="fixed inset-0 bg-white z-50 flex items-center justify-center">
        <div class="animate-spin rounded-full h-32 w-32 border-t-4 border-b-4 border-blue-500"></div>
    </div>
    
    <!-- Navigation -->
    <nav class="fixed w-full glass-effect py-4 z-40">
        <div class="container mx-auto px-6 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold gradient-text">DevPort</a>
            <div class="hidden md:flex space-x-8">
                <a href="#home" class="text-gray-800 hover:text-blue-500 transition">Home</a>
                <a href="#about" class="text-gray-800 hover:text-blue-500 transition">About</a>
                <a href="#skills" class="text-gray-800 hover:text-blue-500 transition">Skills</a>
                <a href="#projects" class="text-gray-800 hover:text-blue-500 transition">Projects</a>
                <a href="#contact" class="text-gray-800 hover:text-blue-500 transition">Contact</a>
            </div>
            <button id="mobile-menu-button" class="md:hidden text-gray-800 focus:outline-none">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-lg rounded-lg mt-2 py-2 absolute right-6 w-48">
            <a href="#home" class="block px-4 py-2 text-gray-800 hover:bg-blue-50">Home</a>
            <a href="#about" class="block px-4 py-2 text-gray-800 hover:bg-blue-50">About</a>
            <a href="#skills" class="block px-4 py-2 text-gray-800 hover:bg-blue-50">Skills</a>
            <a href="#projects" class="block px-4 py-2 text-gray-800 hover:bg-blue-50">Projects</a>
            <a href="#contact" class="block px-4 py-2 text-gray-800 hover:bg-blue-50">Contact</a>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-16">
        <div class="absolute inset-0 z-0">
            <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-br from-blue-50 to-purple-50 opacity-90"></div>
            <div class="absolute top-20 left-20 w-64 h-64 bg-blue-400 rounded-full filter blur-3xl opacity-20 animate-float"></div>
            <div class="absolute bottom-20 right-20 w-64 h-64 bg-purple-400 rounded-full filter blur-3xl opacity-20 animate-float-reverse"></div>
        </div>
        
        <div class="container mx-auto px-6 z-10">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-5xl md:text-7xl font-bold mb-6">
                        Hi, I'm <span class="gradient-text">Seymur</span>
                    </h1>
                    <h2 class="text-2xl md:text-3xl font-semibold text-gray-600 mb-6">
                        Full Stack Developer
                    </h2>
                    <p class="text-gray-600 mb-8 max-w-lg">
                        I build exceptional digital experiences that are fast, accessible, visually appealing, and responsive.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#contact" class="bg-blue-500 hover:bg-blue-600 text-white px-6 py-3 rounded-lg font-medium transition transform hover:-translate-y-1 shadow-lg">
                            Contact Me
                        </a>
                        <a href="#projects" class="border-2 border-blue-500 text-blue-500 hover:bg-blue-50 px-6 py-3 rounded-lg font-medium transition transform hover:-translate-y-1">
                            View Work
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative w-64 h-64 md:w-80 md:h-80">
                        <div class="absolute inset-0 bg-blue-500 rounded-full opacity-20 animate-pulse-slow"></div>
                        <div class="absolute inset-4 bg-gradient-to-br from-blue-400 to-purple-500 rounded-full shadow-xl flex items-center justify-center overflow-hidden">
                            <img src="c:\Users\LocUser\Downloads\IMG-20250613-WA0016.jpg" alt="Seymur Yusubov" class="w-full h-full object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <a href="#about" class="text-gray-600 hover:text-blue-500">
                <i class="fas fa-chevron-down text-2xl"></i>
            </a>
        </div>
    </section>
    
    <!-- About Section -->
    <section id="about" class="py-20 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4">About <span class="gradient-text">Me</span></h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto"></div>
            </div>
            
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/3 mb-10 md:mb-0 flex justify-center">
                    <div class="relative w-64 h-64 rounded-full overflow-hidden shadow-xl border-4 border-white">
                        <img src="c:\Users\LocUser\Downloads\1294266.webp" alt="Seymur Yusubov" class="w-full h-full object-cover">
                    </div>
                </div>
                <div class="md:w-2/3 md:pl-12">
                    <h3 class="text-2xl font-semibold mb-4">Who am I?</h3>
                    <p class="text-gray-600 mb-6">
                        I'm Seymur Yusubov, a passionate Full Stack Developer with expertise in modern web technologies. 
                        I specialize in creating responsive, user-friendly websites and applications that deliver 
                        exceptional user experiences.
                    </p>
                    <p class="text-gray-600 mb-6">
                        With a strong foundation in both front-end and back-end development, I bring ideas to life 
                        through clean, efficient code and innovative solutions. My goal is to build products that 
                        not only meet but exceed client expectations.
                    </p>
                    </a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Skills Section -->
    <section id="skills" class="py-20 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4">My <span class="gradient-text">Skills</span></h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-html5 text-3xl text-orange-500"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">HTML5</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-orange-500 h-2.5 rounded-full" style="width: 95%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-css3-alt text-3xl text-blue-500"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">CSS3</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-blue-500 h-2.5 rounded-full" style="width: 90%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-js text-3xl text-yellow-500"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">JavaScript</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-yellow-500 h-2.5 rounded-full" style="width: 85%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-react text-3xl text-blue-400"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">React</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-blue-400 h-2.5 rounded-full" style="width: 80%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-node-js text-3xl text-green-500"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Node.js</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-green-500 h-2.5 rounded-full" style="width: 75%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-database text-3xl text-blue-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">MongoDB</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-blue-600 h-2.5 rounded-full" style="width: 70%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fab fa-git-alt text-3xl text-orange-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Git</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-orange-600 h-2.5 rounded-full" style="width: 85%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition text-center">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-mobile-alt text-3xl text-purple-500"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Responsive Design</h3>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-purple-500 h-2.5 rounded-full" style="width: 90%"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4">My <span class="gradient-text">Projects</span></h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card bg-white rounded-xl overflow-hidden shadow-lg transition duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="c:\Users\LocUser\Downloads\wp2945934.webp" alt="Project 1" class="w-full h-full object-cover transition duration-500 hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent flex items-end p-4">
                            <h3 class="text-white text-xl font-semibold">E-commerce Platform</h3>
                        </div>
                    </div>
                    <div class="p-6">
                        <p class="text-gray-600 mb-4">A full-featured e-commerce platform with payment integration, product management, and user authentication.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 text-blue-800 text-xs px-3 py-1 rounded-full">React</span>
                            <span class="bg-green-100 text-green-800 text-xs px-3 py-1 rounded-full">Node.js</span>
                            <span class="bg-yellow-100 text-yellow-800 text-xs px-3 py-1 rounded-full">MongoDB</span>
                        </div>
                        <div class="flex space-x-3">
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-blue-500 hover:text-blue-700">
                                <i class="fas fa-external-link-alt"></i> Live Demo
                            </a>
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-gray-600 hover:text-gray-800">
                                <i class="fab fa-github"></i> Code
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card bg-white rounded-xl overflow-hidden shadow-lg transition duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="c:\Users\LocUser\Downloads\wp5085063.jpg" alt="Project 2" class="w-full h-full object-cover transition duration-500 hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent flex items-end p-4">
                            <h3 class="text-white text-xl font-semibold">Task Management App</h3>
                        </div>
                    </div>
                    <div class="p-6">
                        <p class="text-gray-600 mb-4">A productivity application for managing tasks with drag-and-drop functionality and team collaboration features.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-100 text-blue-800 text-xs px-3 py-1 rounded-full">Vue.js</span>
                            <span class="bg-purple-100 text-purple-800 text-xs px-3 py-1 rounded-full">Firebase</span>
                            <span class="bg-pink-100 text-pink-800 text-xs px-3 py-1 rounded-full">Tailwind CSS</span>
                        </div>
                        <div class="flex space-x-3">
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-blue-500 hover:text-blue-700">
                                <i class="fas fa-external-link-alt"></i> Live Demo
                            </a>
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-gray-600 hover:text-gray-800">
                                <i class="fab fa-github"></i> Code
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card bg-white rounded-xl overflow-hidden shadow-lg transition duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="c:\Users\LocUser\Downloads\wp2821120.webp" alt="Project 3" class="w-full h-full object-cover transition duration-500 hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent flex items-end p-4">
                            <h3 class="text-white text-xl font-semibold">Social Media Dashboard</h3>
                        </div>
                    </div>
                    <div class="p-6">
                        <p class="text-gray-600 mb-4">A comprehensive dashboard for managing multiple social media accounts with analytics and scheduling features.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-400 text-white text-xs px-3 py-1 rounded-full">React</span>
                            <span class="bg-gray-800 text-white text-xs px-3 py-1 rounded-full">Next.js</span>
                            <span class="bg-blue-600 text-white text-xs px-3 py-1 rounded-full">TypeScript</span>
                        </div>
                        <div class="flex space-x-3">
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-blue-500 hover:text-blue-700">
                                <i class="fas fa-external-link-alt"></i> Live Demo
                            </a>
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="text-gray-600 hover:text-gray-800">
                                <i class="fab fa-github"></i> Code
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" class="inline-block bg-blue-500 hover:bg-blue-600 text-white px-6 py-3 rounded-lg font-medium transition shadow-lg">
                    View All Projects
                </a>
            </div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4">Get In <span class="gradient-text">Touch</span></h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto"></div>
            </div>
            
            <div class="flex flex-col lg:flex-row gap-12">
                <div class="lg:w-1/2">
                    <h3 class="text-2xl font-semibold mb-6">Contact Information</h3>
                    <p class="text-gray-600 mb-8">
                        Feel free to reach out to me for any questions or opportunities. I'm always open to discussing new projects, creative ideas, or opportunities to be part of your vision.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="bg-blue-100 p-3 rounded-full mr-4">
                                <i class="fas fa-envelope text-blue-500"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">Email</h4>
                                <a href="mailto:yusubovseymur237@gmail.com" class="text-gray-600 hover:text-blue-500">yusubovseymur237@gmail.com</a>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-blue-100 p-3 rounded-full mr-4">
                                <i class="fab fa-instagram text-blue-500"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">Instagram</h4>
                                <a href="https://instagram.com/the.usbv" target="_blank" class="text-gray-600 hover:text-blue-500">@the.usbv</a>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-blue-100 p-3 rounded-full mr-4">
                                <i class="fab fa-github text-blue-500"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800">GitHub</h4>
                                <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" target="_blank" class="text-gray-600 hover:text-blue-500">github.com/seymurdeveloper</a>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-10">
                        <h4 class="font-semibold text-gray-800 mb-4">Follow Me</h4>
                        <div class="flex space-x-4">
                            <a href="https://instagram.com/the.usbv" target="_blank" class="social-icon bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center text-blue-500 hover:bg-blue-500 hover:text-white">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" target="_blank" class="social-icon bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center text-blue-500 hover:bg-blue-500 hover:text-white">
                                <i class="fab fa-github"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="lg:w-1/2">
                    <form id="contactForm" class="bg-white p-8 rounded-xl shadow-lg">
                        <div class="mb-6">
                            <label for="name" class="block text-gray-700 font-medium mb-2">Your Name</label>
                            <input type="text" id="name" name="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" required>
                        </div>
                        
                        <div class="mb-6">
                            <label for="email" class="block text-gray-700 font-medium mb-2">Your Email</label>
                            <input type="email" id="email" name="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" required>
                        </div>
                        
                        <div class="mb-6">
                            <label for="subject" class="block text-gray-700 font-medium mb-2">Subject</label>
                            <input type="text" id="subject" name="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" required>
                        </div>
                        
                        <div class="mb-6">
                            <label for="message" class="block text-gray-700 font-medium mb-2">Your Message</label>
                            <textarea id="message" name="message" rows="5" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" required></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-blue-500 hover:bg-blue-600 text-white py-3 px-6 rounded-lg font-medium transition shadow-lg">
                            Send Message
                        </button>
                        
                        <div id="formMessage" class="mt-4 text-center hidden"></div>
                    </form>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <a href="#" class="text-2xl font-bold gradient-text">Seymur Yusubov</a>
                    <p class="text-gray-400 mt-2">Creating digital experiences that matter.</p>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 Seymur Yusubov. All rights reserved.
                </p>
                
                <div class="flex space-x-4">
                    <a href="https://instagram.com/the.usbv" target="_blank" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="https://github.com/seymurdeveloper/seymurdeveloper.git" target="_blank" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-github"></i>
                    </a>
                </div>
            </div>
        </div>
    </footer>
    
    <script>
        // Loading screen
        window.addEventListener('load', function() {
            setTimeout(function() {
                document.getElementById('loading').style.opacity = '0';
                setTimeout(function() {
                    document.getElementById('loading').style.display = 'none';
                }, 500);
            }, 1000);
        });
        
        // Mobile menu toggle
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });
        
        // Close mobile menu when clicking outside
        document.addEventListener('click', function(event) {
            const menuButton = document.getElementById('mobile-menu-button');
            const menu = document.getElementById('mobile-menu');
            
            if (!menu.contains(event.target) && event.target !== menuButton) {
                menu.classList.add('hidden');
            }
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    document.getElementById('mobile-menu').classList.add('hidden');
                }
            });
        });
        
        // Cursor effect
        const cursor = document.getElementById('cursor');
        
        document.addEventListener('mousemove', (e) => {
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
        });
        
        // Add hover effect to interactive elements
        const interactiveElements = document.querySelectorAll('a, button, input, textarea, .project-card, .social-icon');
        
        interactiveElements.forEach(el => {
            el.addEventListener('mouseenter', () => {
                cursor.style.transform = 'translate(-50%, -50%) scale(1.5)';
                cursor.style.backgroundColor = 'rgba(59, 130, 246, 0.5)';
                cursor.style.borderColor = 'transparent';
            });
            
            el.addEventListener('mouseleave', () => {
                cursor.style.transform = 'translate(-50%, -50%) scale(1)';
                cursor.style.backgroundColor = 'transparent';
                cursor.style.borderColor = '#3B82F6';
            });
        });
        
        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const form = this;
            const formData = new FormData(form);
            const formMessage = document.getElementById('formMessage');
            
            // Simulate form submission (in a real scenario, you would use fetch or XMLHttpRequest)
            setTimeout(() => {
                formMessage.textContent = 'Your message has been sent successfully! I will get back to you soon.';
                formMessage.classList.remove('hidden', 'text-red-500');
                formMessage.classList.add('text-green-500');
                
                // Send email (in a real scenario, you would need a backend service)
                const emailBody = `Name: ${formData.get('name')}\nEmail: ${formData.get('email')}\nSubject: ${formData.get('subject')}\nMessage: ${formData.get('message')}`;
                const mailtoLink = `mailto:yusubovseymur237@gmail.com?subject=New Message from Portfolio&body=${encodeURIComponent(emailBody)}`;
                
                // Open email client (this is a fallback, in production you would use a server-side solution)
                window.location.href = mailtoLink;
                
                form.reset();
            }, 1000);
        });
        
        // Animation on scroll
        const animateOnScroll = function() {
            const elements = document.querySelectorAll('.project-card, .skill-card');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementPosition < windowHeight - 100) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        };
        
        // Initialize elements with opacity 0 and slight offset
        document.querySelectorAll('.project-card, .skill-card').forEach(element => {
            element.style.opacity = '0';
            element.style.transform = 'translateY(20px)';
            element.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
