# 🎠 Pure CSS Carousel/Slider

A **fully functional image carousel** that cycles through slides **automatically and manually** using **only CSS**. This slider supports:
- **Manual navigation** via radio buttons.
- **Automatic sliding** using `@keyframes` animations.
- **Responsive design** that adapts to different screen sizes.
- **No JavaScript required!**

---

## 🚀 Features  
- ✅ **Pure CSS Implementation** (No JavaScript)  
- 🎨 **Smooth Slide Transitions**  
- 🔄 **Automatic and Manual Sliding Options**  
- 📌 **Radio Button Hack for Manual Control**  
- 📱 **Fully Responsive for Mobile & Desktop**  

---

## 🏗️ HTML Structure  
- **`<input type="radio" id="slide1">`**: Hidden radio buttons to toggle slides.
- **`<label for="slide1">`**: Clickable labels act as slide selectors.
- **`<div class="slides-container">`**: Wrapper holding slide images.
- **`@keyframes autoSlide`**: Enables automatic transitions.

---

## 🎨 CSS Styling Used  
- **Global Reset**: Ensures consistency across browsers.  
- **Carousel Behavior**:  
  - **Manual Mode**: Clicking radio buttons updates slide position.  
  - **Auto Mode**: Uses `@keyframes` to cycle through slides.  
- **Smooth Transitions**: Uses `transform: translateX()` for animations.  
- **Navigation Dots**: Highlights the active slide.  

---

## 🎬 How It Works  

### 📌 **Manual Sliding (Radio Buttons + CSS Selectors)**  
- Users select a slide by clicking a **radio button**.
- CSS updates `transform: translateX(-100%)` based on `:checked`.
- No JavaScript is needed!

```css
#slide1:checked ~ .slides-container { transform: translateX(0%); }
#slide2:checked ~ .slides-container { transform: translateX(-100%); }
#slide3:checked ~ .slides-container { transform: translateX(-200%); }
```

### 🎞️ **Automatic Sliding (Keyframes Animation)**  
- Uses `@keyframes autoSlide` to shift slides every few seconds.
- The animation loops infinitely.

```css
@keyframes autoSlide {
    0%, 30% { transform: translateX(0%); }
    33%, 63% { transform: translateX(-100%); }
    66%, 96% { transform: translateX(-200%); }
    100% { transform: translateX(0%); }
}
```

```css
.slides-container-2 {
    animation: autoSlide 15s infinite;
}
```

---

## 📱 Responsive Behavior  
- **Desktop**: Smooth sliding with responsive layout.  
- **Mobile**: Adapts to smaller screens for better user experience.  

---

## 📷 Screenshots  
### 🖥️ **Desktop Preview**  
![Desktop Preview](Assets/desktop.png)  


---



