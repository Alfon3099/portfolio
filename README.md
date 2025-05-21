Page Link 

Interactive Function

JS

1. Dynamic Navigation Highlighting on Scroll

Functionality: Highlights the nav link corresponding to the section currently visible in the viewport.

JS Code:const sections = document.querySelectorAll("section");
const navLinks = document.querySelectorAll("nav a");

window.addEventListener("scroll", () => {
  let currentSection = "";
  sections.forEach((section) => {
    const sectionTop = section.offsetTop - 60; 
    if (window.scrollY >= sectionTop) {
      currentSection = section.getAttribute("id");
    }
  });

  navLinks.forEach((link) => {
    link.classList.remove("active");
    if (link.getAttribute("href") === `#${currentSection}`) {
      link.classList.add("active");
    }
  });
});

CSS 

1. Smooth Scrolling Behavior

Functionality: Smoothly scrolls to sections when clicking navigation links.

CSS Code: body {
  scroll-behavior: smooth;
}

2. Navigation Link Hover and Active Effect

Functionality: Changes background and text color of nav links on hover or when active.

CSS Code:nav a {
  color: #a0d9ffcc;
  padding: 0.5em 0.6em;
  border-radius: 6px;
  transition: background-color 0.3s ease, color 0.3s ease;
}
nav a.active,
nav a:hover {
  background: #00aaffcc;
  color: #001f30;
  box-shadow: 0 0 10px #00aaffbb;
}

3. Profile Picture Hover Animation
Functionality: Enlarges and rotates profile picture slightly on hover.

CSS Code: #profile img:hover {
  transform: scale(1.12) rotate(5deg);
}

4. Card Hover Effect (Projects/Trainings)

Functionality: Lifts the card, changes background and text color on hover.

CSS Code: .card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 18px #00c7ffbb;
  background: #007bb8;
  color: #ccf7ff;
}

5. Job Experience Hover Effect

Functionality: Enlarges and changes background color of job card on hover.

CSS Code: #job-experience li:hover {
  background: #0099cc;
  transform: scale(1.05);
  color: #def8ff;
}

6. Education List Hover Highlight

Functionality: Highlights and changes text color of education list items on hover.

CSS Code: #education li:hover {
  background: #007bb8cc;
  color: #cdefff;
}

7. Form Field Focus Effects
Functionality: Glows input and textarea fields when they’re focused.

CSS Code: #contact input[type="text"]:focus,
#contact input[type="email"]:focus,
#contact textarea:focus {
  box-shadow: 0 0 8px #00c7ffcc;
}


