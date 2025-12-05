// ===== DOM ELEMENTS =====
const header = document.getElementById('header');
const mobileToggle = document.getElementById('mobileToggle');
const mobileMenu = document.getElementById('mobileMenu');
const backToTop = document.getElementById('backToTop');
const progressBar = document.getElementById('progressBar');
const faqItems = document.querySelectorAll('.faq-item');
const reveals = document.querySelectorAll('.reveal');

// ===== MOBILE MENU =====
mobileToggle.addEventListener('click', () => {
    mobileMenu.classList.toggle('active');
    const icon = mobileToggle.querySelector('i');
    if (mobileMenu.classList.contains('active')) {
        icon.classList.remove('fa-bars');
        icon.classList.add('fa-times');
    } else {
        icon.classList.remove('fa-times');
        icon.classList.add('fa-bars');
    }
});

// Close mobile menu when clicking a link
mobileMenu.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', () => {
        mobileMenu.classList.remove('active');
        mobileToggle.querySelector('i').classList.remove('fa-times');
        mobileToggle.querySelector('i').classList.add('fa-bars');
    });
});

// ===== HEADER SCROLL BEHAVIOR =====
let lastScrollY = window.scrollY;

window.addEventListener('scroll', () => {
    const currentScrollY = window.scrollY;
    
    // Show/hide header
    if (currentScrollY > 100) {
        if (currentScrollY > lastScrollY) {
            header.classList.add('hidden');
        } else {
            header.classList.remove('hidden');
        }
    } else {
        header.classList.remove('hidden');
    }
    
    lastScrollY = currentScrollY;
    
    // Progress bar
    const scrollHeight = document.documentElement.scrollHeight - window.innerHeight;
    const scrollProgress = (currentScrollY / scrollHeight) * 100;
    progressBar.style.width = scrollProgress + '%';
    
    // Back to top button
    if (currentScrollY > 500) {
        backToTop.classList.add('visible');
    } else {
        backToTop.classList.remove('visible');
    }
});

// ===== BACK TO TOP =====
backToTop.addEventListener('click', () => {
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    });
});

// ===== REVEAL ON SCROLL =====
function revealOnScroll() {
    reveals.forEach(element => {
        const elementTop = element.getBoundingClientRect().top;
        const windowHeight = window.innerHeight;
        
        if (elementTop < windowHeight - 100) {
            element.classList.add('active');
        }
    });
}

window.addEventListener('scroll', revealOnScroll);
window.addEventListener('load', revealOnScroll);

// ===== FAQ ACCORDION =====
faqItems.forEach(item => {
    const question = item.querySelector('.faq-question');
    
    question.addEventListener('click', () => {
        // Close other items
        faqItems.forEach(otherItem => {
            if (otherItem !== item) {
                otherItem.classList.remove('active');
            }
        });
        
        // Toggle current item
        item.classList.toggle('active');
    });
});

// ===== SMOOTH SCROLL FOR ANCHOR LINKS =====
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// ===== ANIMATE NUMBERS (Optional) =====
function animateValue(element, start, end, duration) {
    let startTimestamp = null;
    const step = (timestamp) => {
        if (!startTimestamp) startTimestamp = timestamp;
        const progress = Math.min((timestamp - startTimestamp) / duration, 1);
        element.textContent = Math.floor(progress * (end - start) + start);
        if (progress < 1) {
            window.requestAnimationFrame(step);
        }
    };
    window.requestAnimationFrame(step);
}

// ===== CONSOLE MESSAGE =====
console.log('%c⚡ Virtus Elite', 'color: #E8E7D2; font-size: 24px; font-weight: bold;');
console.log('%cTransformando conteúdo em clientes.', 'color: #888; font-size: 14px;');
