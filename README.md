

Welcome to my personal portfolio! This is a fully responsive webpage designed using only HTML and CSS, highlighting my programming journey and skills.

Project Structure

Structure of the Website : index.html 

Home section: 

<img width="1806" height="917" alt="Screenshot from 2025-07-20 22-02-37" src="https://github.com/user-attachments/assets/4c86368f-1563-4009-a9a1-425bf57f0bda" />


	1. <head> Section: 
 Sets the viewport, title, and links external stylesheets:
        ◦ AOS for animation effects.
        ◦ Boxicons for social/media icons.
        ◦ Custom style.css.
Code :
```
<link rel="stylesheet" href="style.css" />
```

	2. <video> Background: here a looping video is added as the background. 

Code: 
```
<video autoplay loop muted plays-inline class="back-vid">
  <source src="images/galaxy.mp4" type="video/mp4" />
</video>
```



	3. Navigation Menu:
Here the navigations menu’s are created with the tag nav. Here using section-id within the href ensures the navigation buttons links to the respective sections.
Uses flexbox to align navigation links.

Code: 
```
 <nav>
      <ul>
        <li><a class="active" href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
	
```
4. Hero Section:

	The term comes from graphic design and advertising — where a "hero image" is the big, bold image or message that draws attention.





Code: 
```
<div class="hero">
  <div class="hero-info">
    <h1>Hi, I'm UMME ZOAYRIA ABEDIN</h1>
    <h2>I'm a PROGRAMMER</h2>
   ...
  </div>

  <div class="hero-img">
    <img src="images/portfolioIMG.png" alt="person-img" />
  </div>
</div>
```

Left side contains an intro message with animations.
Right side shows a circular profile image with glowing hover effects.


Styling & Effects : style.css 

	1. Base Styles:
Code : 
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
```
Sets default spacing and font for a consistent layout.

	2. Background Video:
Code: 
```
.back-vid {
  position: absolute;
  left: 0;
  top: 0;
  z-index: -1;
}
```
Positioned behind all content using z-index: -1.




	3. Navigation Bar:
Code: 
```
nav {
  display: flex;
  justify-content: space-between;
  padding: 30px 40px;
}
nav a:hover, .active {
  color: #4acfee;
  text-decoration: underline;
}
```
Flexbox ensures responsive layout. Hover effects highlight the link.

	4. Hero Section:
Code: 
```
.hero {
  display: flex;
  justify-content: space-between;
  padding: 60px 10%;
}
.hero h1 {
  font-size: 72px;
  font-weight: 900;
}
```
Large text and space create a professional look. Responsive tweaks included using @media queries.

	5. Profile Image:
Code: 
```
.hero-img {
  width: 400px;
  height: 400px;
  border-radius: 50%;
  box-shadow: 0 0 10px #4eddfd;
}
```
Circular profile picture with a glowing border on hover.

About me: 

<img width="1806" height="917" alt="Screenshot from 2025-07-20 22-02-48" src="https://github.com/user-attachments/assets/d2074a9a-2c6f-48d8-9267-91e1aaa4488c" />

Code :
```
<section id="about" class="content-section">
    <h2>About Me</h2>
    <p>I am a 3rd-year CSE student at Shahjalal University of Science and Technology, Sylhet; passionate about AI, machine learning, and full-stack development. I love solving problems and learning new technologies.</p>
  </section>
```

Here section tag is used to create an individual section. The id="about" allows to create clickable links (like in the navbar) that scroll to this exact section on the page. The id is a unique name in the entire HTML file.
It identifies the section semantically and structurally.
The class content-section is used to apply shared CSS styles to multiple sections. Whereas, id="about" is a unique name (used for navigation), class="content-section" applies common layout and design styles.

Styling of Sections:
Code:
```
.content-section {
  min-height: 100vh;
  padding: 120px 10%;
  background-color: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(5px);
  color: white;
  border-top: 2px solid #4acfee44;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
```
Explanation: 

| Property                                                                  | Effect                                                                              |
| ------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `min-height: 100vh;`                                                      | Makes the section take **full screen height**, even if content is small.            |
| `padding: 120px 10%;`                                                     | Adds space **inside** the section (top/bottom = 120px, left/right = 10% of screen). |
| `background-color: rgba(255, 255, 255, 0.02);`                            | Very light **transparent white background**. Gives a subtle glass effect.           |
| `backdrop-filter: blur(5px);`                                             | Adds a **blur effect** to the background video beneath it.                          |
| `color: white;`                                                           | Makes all text inside the section **white**.                                        |
| `border-top: 2px solid #4acfee44;`                                        | Adds a **semi-transparent cyan border** line at the top of the section.             |
| `display: flex;` + `flex-direction: column;` + `justify-content: center;` | Vertically centers the content using **Flexbox layout**.                            |



<h1>Styling of <h2> Inside .content-section:</h1>

```
.content-section h2 {
  font-size: 50px;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-bottom: 30px;

  background: linear-gradient(to right, #4acfee, #53f8c9, #6070fd);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  animation: animate-gradient 4s linear infinite;
}
```

What Each Style Does:

| Property                                     | Effect                                                              |
| -------------------------------------------- | ------------------------------------------------------------------- |
| `font-size`, `font-weight`, `text-transform` | Makes it **bold**, **uppercase**, and **large**.                    |
| `letter-spacing: 1.5px;`                     | Adds spacing between letters for readability.                       |
| `background: linear-gradient(...)`           | Applies a **gradient color** to the text.                           |
| `background-clip: text` & `-webkit-...`      | Makes the gradient **visible inside the text**, not the background. |
| `text-fill-color: transparent`               | Removes the default black text color so the gradient is visible.    |
| `animation: animate-gradient ...`            | Animates the gradient so it appears to move or shimmer.             |

This is why "ABOUT ME" heading has that animated blue-to-purple shimmer effect.

 <h1>Styling of Inside .content-section</h1>
Code: 

```
.content-section p {
  font-size: 20px;
  line-height: 1.9;
  color: #e8f1f8;
  font-weight: 400;
  letter-spacing: 0.5px;
  animation: fadeInUp 1s ease-out both;
}
```

This adds:
| Property                   | Effect                                                                 |
| -------------------------- | ---------------------------------------------------------------------- |
| `font-size`, `line-height` | Makes paragraph text **easy to read** and well-spaced.                 |
| `color: #e8f1f8`           | Gives a **softer white** color (not too harsh like pure white).        |
| `letter-spacing: 0.5px`    | Adds slight spacing for readability.                                   |
| `animation: fadeInUp`      | Makes the paragraph **fade in and move upward** when it first appears. |


<h1> Animation Defined in CSS:</h1> 
Code: 

```
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
```
Smoothly transitions the paragraph from invisible and below to visible and in place.


<h1>Projects</h1>

<img width="1806" height="917" alt="Screenshot from 2025-07-20 22-02-59" src="https://github.com/user-attachments/assets/0b22cf8c-4379-420e-b8aa-0aa87ab6af93" />

Html Code:
```
<section id="projects" class="content-section">
    <h2>Projects</h2>
    <ul>
      <li><strong>Compiler</strong> 
        <a href="https://github.com/delwar03/go-dfz" target="_blank" style="color:#4acfee; text-decoration: underline;">
          A compiler built with Python.
        </a> </li>
      <li><strong>ScanShot</strong>
        <a href="https://github.com/ZoayriaAbedin/project2-2" target="_blank" style="color:#4acfee; text-decoration: underline;">
          An android app built to convert image to text and detect objects using ML kits.
        </a> </li>
    </ul>
  </section>
  ```

Here <a> tags are links to GitHub projects. Inside the list items are using inline styles:
```
style="color:#4acfee; text-decoration: underline;"
```
So they appear:

In cyan (#4acfee) — matching theme.
Underlined — ensuring it looks clickable and accessible.


<h1>Skills</h1>

<img width="1806" height="917" alt="Screenshot from 2025-07-20 22-03-10" src="https://github.com/user-attachments/assets/537c17c7-af0d-4e6c-9228-47fa46d34822" />

Html Code :
```
<section id="skills" class="content-section">
  <h2>Skills</h2>
  <p>
    Languages: C/C++, Java, Python <br/>
    Tools: Git, Android Studio, VS Code<br/>
    Technologies: REST API<br/>
    CP: 
    <a href="https://codeforces.com/profile/Zoyria" target="_blank" style="color:#4acfee; text-decoration: underline;">
      Codeforces
    </a> and 
    <a href="https://vjudge.net/user/2021331042" target="_blank" style="color:#4acfee; text-decoration: underline;">
      VJudge
    </a>
  </p>
</section>
```

Here,  <a>	Links to competitive programming profiles (Codeforces & VJudge)


<h1>Contacts</h1>
<img width="1806" height="917" alt="Screenshot from 2025-07-20 22-03-17" src="https://github.com/user-attachments/assets/73408770-9347-4d4e-9557-5e64a38610cd" />


Html Code:
```
<section id="contact" class="content-section">
    <h2>Contact</h2>
    <p>Phone: 01934347283 <br/>Email: 2021331042@student.sust.edu<br/>GitHub: github.com/ZoayriaAbedin<br/>LinkedIn: linkedin.com/in/zoayria-abedin-74a93a299</p>
    <div class="Buttons">
      <ul class="ul-icons">
       <!-- <li><a href="mailto:2021331042@student.sust.edu"><i class='bx bxl-gmail'></i></a></li>-->
        <li><a href="https://github.com/ZoayriaAbedin"><i class='bx bxl-github'></i></a></li>
        <li><a href="https://www.linkedin.com/in/zoayria-abedin-74a93a299/"><i class='bx bxl-linkedin'></i></a></li>
               
        </li>   
      </ul>
    </div>
  </section>
```
Here contacts infos are added and a list of clickable icons (GitHub, LinkedIn) added using Boxicons.

Css Style:

Code:
```
.ul-icons {
  list-style: none;
  display: flex;
  gap: 20px;
  padding: 0;
  margin-top: 20px;
}

.ul-icons li a {
  font-size: 28px;
  color: #4acfee;
  transition: transform 0.2s ease;
}

.ul-icons li a:hover {
  transform: scale(1.2);
}
```


| Rule                             | Purpose                            |
| -------------------------------- | ---------------------------------- |
| `list-style: none;`              | Removes bullet points              |
| `display: flex; gap: 20px;`      | Aligns icons in a row with spacing |
| `font-size: 28px;`               | Makes icons large and visible      |
| `color: #4acfee;`                | Cyan color to match your theme     |
| `transform: scale(1.2)` on hover | Adds smooth hover zoom effect      |




At the end of the file
```
<script src="https://unpkg.com/aos@next/dist/aos.js"></script>
<script>AOS.init();</script>
```
loads and activates AOS — a JavaScript library called Animate On Scroll (AOS).






  





