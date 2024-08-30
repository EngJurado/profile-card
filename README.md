# Profile Card

![Astro](https://img.shields.io/badge/astro-%232C2052.svg?style=for-the-badge&logo=astro&logoColor=white)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

## Overview

This project is a web application built using Astro, designed to create a profile card with social media links. It includes various components and utilities to build a responsive and interactive user interface. The template allows for easy integration of multiple social links, enhancing user connectivity.

![mockup](https://github.com/EngJurado/profile-card/blob/main/mockup.jpg)

## Folder Structure

```
src/
├── components/
│   └── Card.astro
├── images/
│   └── profile.webp
├── layouts/
│   └── Layout.astro
└── pages/
    └── index.astro
```

### Components
- **components/Card.astro**: A card component used to display the profile card with social media links.

### Images
- **images/profile.webp**: The profile image used in the profile card.

### Layouts
- **layouts/Layout.astro**: The layout component for the application.

### Pages
- **pages/index.astro**: The main landing page of the application.

## Customization

Edit this data in src/pages/index.astro

- **`title`**: This change will be reflected in the browser tab.
- **`description`**: This is a metadata tag used to provide a brief description of your page in search engines.
- **`name`**: Enter your name here.
- **`position`**: Enter your job position here.
- **`about me`**: Write a brief description of who you are and what you do. It's recommended to keep it under 540 characters.
- **`linkedin`**, **`github`**, **`telegram`** and **`x`**: Enter the URLs to your personal pages here.
- **`cvLink`**: Provide the URL to your resume in PDF format for download or insert it in /public/files/resume-cv.pdf
- **`profileImage`**: Upload your professional profile picture here.

To use more social links, copy and paste this block of code in /src/components/Card.astro file in the position of your desire inside the card.

```sh
<a href={twitterx} class="hover-text" target="_blank">
    <span class="tooltip-text" id="fade">
        Twitter/X
    </span>
    <i class="bi bi-twitter-x"></i>
</a>
````
Change the icon by modifying **`bi-new-icon`** to an icon from the [Bootstrap Website](https://icons.getbootstrap.com).

Then rename the variable newSocialLink in **`<a href={newSocialLink} class="hover-text" target="_blank">`**, and add the new variable in **`const {name, position, aboutMe, linkedin, github, telegram, twitterx, newSocialLink, cvLink } = Astro.props;`**.

Add the new variable in /src/pages/index.astro below the existing social links.

```sh
<Card	name="Carlos Jurado"
    position="Bioengineering | Brain modulation | Artificial Intelligence"
    aboutMe="Dedicated Bioengineer with expertise in medical devices and neuromodulation, pursuing a Master’s in AI. Experienced at Medtronic in surgical support, neurostimulator programming, and patient safety. Strong analytical skills and problem-solving abilities drive my commitment to innovation and continuous improvement in healthcare."
    linkedin="https://www.linkedin.com/in/engjurado/"
    github="https://github.com/EngJurado"
    telegram="https://telegram.me/engjurado"
    twitterx="https://x.com/EngJurado"
    cvLink="/files/resume-cv.pdf"
/>
```

## Setup and Usage

1. **Clone the repository**:
   ```sh
   git clone https://github.com/EngJurado/profile-card
   cd project-name
   ```

2. **Install dependencies**:
   ```sh
   npm install
   ```

3. **Run the development server**:
   ```sh
   npm run dev
   ```

4. **Build for production**:
   ```sh
   npm run build
   ```

5. **Preview the production build**:
   ```sh
   npm run preview
   ```

## Contributing
Feel free to submit issues and pull requests. Contributions are welcome!

## License
This project is licensed under the MIT License.
