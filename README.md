  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  body { 
    font-family: 'Poppins', sans-serif; 
    background-color: var(--bg-color); 
    color: var(--text-color);
    margin: 0; 
    padding: 0;
    line-height: 1.6;
    transition: background-color 0.3s ease;
    scroll-behavior: smooth;
    overflow-x: hidden;
  }
  
  /* Scrollbar Styling */
  ::-webkit-scrollbar {
    width: 8px;
  }
  
  ::-webkit-scrollbar-track {
    background: var(--bg-color);
  }
  
  ::-webkit-scrollbar-thumb {
    background: var(--accent-color);
    border-radius: 10px;
  }
  
  /* Scroll Progress Indicator */
  .progress-container {
    position: fixed;
    top: 0;
    z-index: 1001;
    width: 100%;
    height: 4px;
  }
  
  .progress-bar {
    height: 4px;
    background: linear-gradient(to right, var(--accent-color), var(--secondary-accent));
    width: 0%;
    border-radius: 0 2px 2px 0;
    box-shadow: 0 1px 3px rgba(0,0,0,0.2);
  }
  
  /* Navbar Styles */
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    background-color: var(--nav-bg);
    box-shadow: 0 2px 20px rgba(0,0,0,0.1);
    padding: 1rem 0;
    transition: all 0.3s ease;
  }
  
  .navbar.scrolled {
    padding: 0.6rem 0;
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 0.9);
  }
  
  .nav-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
  }
  
  .logo {
    font-weight: 700;
    font-size: 1.5rem;
    color: var(--accent-color);
    text-decoration: none;
    position: relative;
    overflow: hidden;
    display: inline-block;
  }
  
  .logo::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background: linear-gradient(to right, var(--accent-color), var(--secondary-accent));
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.5s ease;
  }
  
  .logo:hover::after {
    transform: scaleX(1);
    transform-origin: left;
  }
  
  .nav-links {
    display: flex;
    gap: 2rem;
  }
  
  .nav-links a {
    text-decoration: none;
    color: var(--text-color);
    font-weight: 500;
    position: relative;
    padding: 0.5rem 0;
    transition: color 0.3s ease;
  }
  
  .nav-links a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background: linear-gradient(to right, var(--accent-color), var(--secondary-accent));
    transition: width 0.3s ease;
  }
  
  .nav-links a:hover {
    color: var(--accent-color);
  }
  
  .nav-links a:hover::after {
    width: 100%;
  }
  
  .theme-toggle {
    background: none;
    border: none;
    color: var(--text-color);
    font-size: 1.2rem;
    cursor: pointer;
    margin-left: 1rem;
    transition: transform 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.5rem;
    border-radius: 50%;
    background-color: rgba(0,0,0,0.05);
  }
  
  .theme-toggle:hover {
    transform: rotate(30deg);
  }
  
  .mobile-menu-btn {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    width: 30px;
    height: 20px;
    position: relative;
    z-index: 1002;
  }
  
  .menu-icon {
    width: 100%;
    height: 2px;
    background-color: var(--text-color);
    position: absolute;
    transition: all 0.3s ease;
    left: 0;
  }
  
  .menu-icon:nth-child(1) {
    top: 0;
  }
  
  .menu-icon:nth-child(2) {
    top: 9px;
  }
  
  .menu-icon:nth-child(3) {
    top: 18px;
  }
  
  .mobile-menu-btn.active .menu-icon:nth-child(1) {
    transform: rotate(45deg);
    top: 9px;
  }
  
  .mobile-menu-btn.active .menu-icon:nth-child(2) {
    opacity: 0;
  }
  
  .mobile-menu-btn.active .menu-icon:nth-child(3) {
    transform: rotate(-45deg);
    top: 9px;
  }
  
  .mobile-nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-color: rgba(250, 250, 250, 0.98);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 1001;
    transform: translateY(-100%);
    transition: transform 0.5s ease;
    backdrop-filter: blur(5px);
  }
  
  .mobile-nav.active {
    transform: translateY(0);
  }
  
  .mobile-nav a {
    font-size: 1.8rem;
    margin: 1rem 0;
    color: var(--text-color);
    text-decoration: none;
    position: relative;
    display: inline-block;
    overflow: hidden;
  }
  
  .mobile-nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background-color: var(--accent-color);
    transform: scaleX(0);
    transition: transform 0.3s ease;
  }
  
  .mobile-nav a:hover::after {
    transform: scaleX(1);
  }
  
  /* Hero Section */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding-top: 80px;
    position: relative;
    overflow: hidden;
  }
  
  .hero-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: linear-gradient(135deg, #fafafa 0%, #f2f2f2 100%);
    z-index: -2;
  }
  
  .hero-pattern {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%230099cc' fill-opacity='0.05'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    z-index: -1;
  }
  
  .particle {
    position: absolute;
    border-radius: 50%;
    background: rgba(0, 0, 0, 0.05);
    z-index: -1;
    animation: float 15s infinite ease-in-out;
  }
  
  @keyframes float {
    0%, 100% { transform: translate(0, 0) rotate(0deg); }
    25% { transform: translate(-20px, 20px) rotate(5deg); }
    50% { transform: translate(20px, 40px) rotate(0deg); }
    75% { transform: translate(40px, 10px) rotate(-5deg); }
  }
  
  .hero-container {
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }
  
  .hero-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  
  .hero-greeting {
    color: var(--accent-color);
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    opacity: 0;
    animation: fadeInUp 1s forwards 0.5s;
  }
  
  .hero-greeting::before {
    content: '';
    display: inline-block;
    width: 50px;
    height: 2px;
    background: var(--accent-color);
    margin-right: 1rem;
  }
  
  .hero-title {
    font-size: 3.5rem;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeInUp 1s forwards 0.8s;
  }
  
  .hero-title span {
    display: inline-block;
    position: relative;
    color: var(--accent-color);
  }
  
  .hero-title span::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 10px;
    bottom: 5px;
    left: 0;
    background-color: rgba(0, 153, 204, 0.2);
    z-index: -1;
  }
  
  .hero-about {
    font-size: 1.1rem;
    margin-bottom: 2rem;
    line-height: 1.8;
    opacity: 0;
    animation: fadeInUp 1s forwards 1.1s;
  }
  
  .hero-btn {
    display: inline-block;
    padding: 0.8rem 2rem;
    background: linear-gradient(135deg, var(--accent-color) 0%, var(--secondary-accent) 100%);
    color: white;
    text-decoration: none;
    border-radius: 50px;
    font-weight: 500;
    box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    transition: all 0.3s ease;
    width: fit-content;
    position: relative;
    overflow: hidden;
    z-index: 1;
    opacity: 0;
    animation: fadeInUp 1s forwards 1.4s;
  }
  
  .hero-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 0%;
    height: 100%;
    background: linear-gradient(135deg, var(--secondary-accent) 0%, var(--accent-color) 100%);
    transition: all 0.5s ease;
    z-index: -1;
  }
  
  .hero-btn:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.25);
  }
  
  .hero-btn:hover::before {
    width: 100%;
  }
  
  .hero-image {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    opacity: 0;
    animation: fadeIn 1s forwards 1.7s;
  }
  
  .profile-img-container {
    position: relative;
    width: 350px;
    height: 350px;
  }
  
  .profile-overlay {
    position: absolute;
    top: -20px;
    right: -20px;
    width: 100%;
    height: 100%;
    border: 4px solid var(--accent-color);
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    animation: morphBackground 10s linear infinite;
  }
  
  .profile-outline {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 3px solid var(--accent-color);
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    animation: morph 8s linear infinite;
    opacity: 0.7;
  }
  
  .profile-img {
    position: absolute;
    top: 5%;
    left: 5%;
    width: 90%;
    height: 90%;
    object-fit: cover;
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    box-shadow: 0 15px 50px rgba(0,0,0,0.2);
    animation: morph 8s linear infinite;
    filter: none;
  }
  
  @keyframes morph {
    0%, 100% { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; }
    25% { border-radius: 70% 30% 30% 70% / 70% 70% 30% 30%; }
    50% { border-radius: 30% 70% 70% 30% / 70% 70% 30% 30%; }
    75% { border-radius: 70% 30% 30% 70% / 30% 30% 70% 70%; }
  }
  
  @keyframes morphBackground {
    0%, 100% { border-radius: 40% 60% 60% 40% / 60% 60% 40% 40%; }
    25% { border-radius: 60% 40% 40% 60% / 40% 40% 60% 60%; }
    50% { border-radius: 40% 60% 60% 40% / 40% 40% 60% 60%; }
    75% { border-radius: 60% 40% 40% 60% / 60% 60% 40% 40%; }
  }
  
  @keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
  }
  
  @keyframes fadeInUp {
    0% { opacity: 0; transform: translateY(20px); }
    100% { opacity: 1; transform: translateY(0); }
  }
  
  /* Section Styles */
  .section {
    padding: 5rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
  }
  
  .section-header {
    text-align: center;
    margin-bottom: 4rem;
    position: relative;
  }
  
  .section-title {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: var(--accent-color);
    position: relative;
    display: inline-block;
  }
  
  .section-title::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 10px;
    bottom: 5px;
    left: 0;
    background-color: rgba(0, 153, 204, 0.2);
    z-index: -1;
  }
  
  .section-subtitle {
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto;
    opacity: 0.8;
  }
  
  .section-divider {
    height: 5px;
    width: 70px;
    background: linear-gradient(to right, var(--accent-color), var(--secondary-accent));
    margin: 1rem auto;
    border-radius: 5px;
  }
  
  /* Projects Section */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 2rem;
  }
  
  .project-card {
    position: relative;
    background: var(--card-bg);
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
    height: 300px;
  }
  
  .project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to top, rgba(0,0,0,0.8) 0%, rgba(0,0,0,0) 50%);
    z-index: 1;
    opacity: 0;
    transition: opacity 0.5s ease;
  }
  
  .project-card:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 20px 40px rgba(0,0,0,0.2);
  }
  
  .project-card:hover::before {
    opacity: 1;
  }
  
  .project-content {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 1.5rem;
    z-index: 2;
    transform: translateY(70%);
    transition: transform 0.5s ease;
  }
  
  .project-card:hover .project-content {
    transform: translateY(0);
  }
  
  .project-title {
    margin: 0 0 1rem 0;
    font-size: 1.5rem;
    color: white;
    position: relative;
    padding-bottom: 0.5rem;
  }
  
  .project-title::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 50px;
    height: 3px;
    background: var(--accent-color);
  }
  
  .project-desc {
    color: rgba(255,255,255,0.9);
    height: 0;
    opacity: 0;
    transition: all 0.5s ease;
    overflow: hidden;
  }
  
  .project-card:hover .project-desc {
    height: auto;
    opacity: 1;
    margin-top: 1rem;
  }
  
  .project-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: brightness(0.9) contrast(1.1);
    transition: transform 0.5s ease;
  }
  
  .project-card:hover .project-image {
    transform: scale(1.1);
  }
  
  /* Skills Section */
  .skills-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: center;
  }
  
  .skill-tag {
    background: rgba(0, 0, 0, 0.05);
    color: var(--text-color);
    padding: 0.8rem 1.8rem;
    border-radius: 50px;
    font-weight: 500;
    font-size: 0.9rem;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    border-left: 3px solid var(--accent-color);
    position: relative;
    overflow: hidden;
  }
  
  .skill-tag::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background: linear-gradient(90deg, var(--accent-color) 0%, transparent 100%);
    opacity: 0.1;
    transition: width 0.4s ease;
    z-index: 0;
  }
  
  .skill-tag:hover {
    transform: translateY(-5px) scale(1.05);
    color: black;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  }
  
  .skill-tag:hover::before {
    width: 100%;
  }
  
  /* Timeline for Experience and Education */
  .timeline-container {
    position: relative;
    max-width: 800px;
    margin: 0 auto;
  }
  
  .timeline-container::before {
    content: '';
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 3px;
    height: 100%;
    background: linear-gradient(to bottom, var(--accent-color), var(--secondary-accent));
    border-radius: 5px;
  }
  
  .timeline-item {
    position: relative;
    width: 45%;
    margin: 2rem 0;
    background: var(--card-bg);
    padding: 2rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
  }
  
  .timeline-item:nth-child(odd) {
    margin-right: auto;
  }
  
  .timeline-item:nth-child(even) {
    margin-left: auto;
  }
  
  .timeline-item::before {
    content: '';
    position: absolute;
    top: 50%;
    width: 20px;
    height: 20px;
    background: linear-gradient(135deg, var(--accent-color), var(--secondary-accent));
    border-radius: 50%;
  }
  
  .timeline-item:nth-child(odd)::before {
    right: -10px;
    transform: translateY(-50%) translateX(50%);
  }
  
  .timeline-item:nth-child(even)::before {
    left: -10px;
    transform: translateY(-50%) translateX(-50%);
  }
  
  .timeline-item:hover {
    transform: scale(1.05);
    box-shadow: 0 15px 40px rgba(0,0,0,0.15);
  }
  
  .timeline-date {
    display: inline-block;
    padding: 0.3rem 1rem;
    background: linear-gradient(135deg, var(--accent-color), var(--secondary-accent));
    color: white;
    border-radius: 20px;
    font-size: 0.8rem;
    margin-bottom: 1rem;
  }
  
  .timeline-title {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    color: var(--accent-color);
  }
  
  .timeline-subtitle {
    font-size: 1rem;
    font-weight: 500;
    margin-bottom: 1rem;
  }
  
  /* Certifications Section */
  .certifications-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 2rem;
  }
  
  .certification-card {
    background: var(--card-bg);
    padding: 2rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    cursor: pointer;
  }
  
  .certification-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 4px;
    height: 100%;
    background: linear-gradient(to bottom, var(--accent-color), var(--secondary-accent));
    transition: all 0.3s ease;
  }
  
  .certification-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
  }
  
  .certification-card:hover::before {
    width: 100%;
    opacity: 0.1;
  }
  
  .certification-title {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    color: var(--accent-color);
  }
  
  .certification-issuer {
    font-weight: 500;
    margin-bottom: 1rem;
  }
  
  .certification-date {
    font-size: 0.85rem;
    padding: 0.3rem 0.8rem;
    background: rgba(0, 0, 0, 0.05);
    border-radius: 15px;
    display: inline-block;
  }
  
  /* Contact Section */
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
  }
  
  .contact-card {
    background: var(--card-bg);
    border-radius: 15px;
    padding: 2rem;
    text-align: center;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    z-index: 1;
  }
  
  .contact-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, var(--accent-color), var(--secondary-accent));
    opacity: 0;
    z-index: -1;
    transition: opacity 0.5s ease;
  }
  
  .contact-card:hover {
    transform: translateY(-10px);
    color: white;
  }
  
  .contact-card:hover::before {
    opacity: 1;
  }
  
  .contact-card:hover .contact-icon,
  .contact-card:hover a {
    color: white !important;
  }
  
  .contact-icon {
    font-size: 2.5rem;
    color: var(--accent-color);
    margin-bottom: 1.5rem;
    transition: all 0.3s ease;
  }
  
  .social-links {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    margin-top: 3rem;
  }
  
  .social-link {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: var(--card-bg);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-color);
    font-size: 1.5rem;
    text-decoration: none;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    z-index: 1;
  }
  
  .social-link::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, var(--accent-color), var(--secondary-accent));
    transition: all 0.5s ease;
    opacity: 0;
    z-index: -1;
  }
  
  .social-link:hover {
    color: white;
    transform: translateY(-10px) rotate(360deg);
    box-shadow: 0 20px 30px rgba(0,0,0,0.15);
  }
  
  .social-link:hover::before {
    opacity: 1;
  }
  
  /* Back to Top Button */
  .back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    background: linear-gradient(135deg, var(--accent-color), var(--secondary-accent));
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    cursor: pointer;
    opacity: 0;
    transform: translateY(20px);
    transition: all 0.3s ease;
    z-index: 999;
  }
  
  .back-to-top.show {
    opacity: 1;
    transform: translateY(0);
  }
  
  .back-to-top:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
  }
  
  /* Footer */
  footer {
    background-color: #fafafa;
    padding: 3rem 0;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  
  .footer-content {
    position: relative;
    z-index: 1;
  }
  
  .footer-wave {
    position: absolute;
    top: -80px;
    left: 0;
    width: 100%;
    height: 80px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120' preserveAspectRatio='none'%3E%3Cpath d='M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z' fill='%23ffffff'%3E%3C/path%3E%3C/svg%3E");
    background-size: cover;
  }
  
  .footer-logo {
    font-weight: 700;
    font-size: 1.8rem;
    color: var(--accent-color);
    margin-bottom: 1rem;
    display: inline-block;
  }
  
  .copyright {
    margin-top: 1rem;
    font-size: 0.9rem;
    opacity: 0.8;
  }
  
  /* Media Queries */
  @media (max-width: 992px) {
    .hero-container {
      grid-template-columns: 1fr;
      text-align: center;
    }
    
    .hero-btn {
      margin: 0 auto;
    }
    
    .hero-greeting::before {
      display: none;
    }
    
    .hero-image {
      order: -1;
      margin-bottom: 2rem;
    }
    
    .profile-img-container {
      width: 280px;
      height: 280px;
    }
    
    .timeline-container::before {
      left: 0;
    }
    
    .timeline-item {
      width: 90%;
      margin-left: auto;
    }
    
    .timeline-item::before {
      left: -10px;
      transform: translateY(-50%) translateX(-50%);
    }
  }
  
  @media (max-width: 768px) {
    .nav-links {
      display: none;
    }
    
    .mobile-menu-btn {
      display: block;
    }
    
    .hero-title {
      font-size: 2.5rem;
    }
    
    .section {
      padding: 3rem 1.5rem;
    }
    
    .contact-grid {
      grid-template-columns: 1fr;
    }
  }
  
  @media (max-width: 480px) {
    .nav-container {
      padding: 0 1rem;
    }
    
    .hero-container {
      padding: 0 1rem;
    }
    
    .profile-img-container {
      width: 220px;
      height: 220px;
    }
    
    .section-title {
      font-size: 2rem;
    }
    
    .back-to-top {
      bottom: 20px;
      right: 20px;
      width: 40px;
      height: 40px;
    }
  }
</style>
