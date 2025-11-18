
# Smart Image Slider

A responsive web-based image slider with dynamic content management and playback controls.

## 📁 Project Structure

```
project-root/
├── index.html
└── README.md
```

## 📋 Features

### Core Functionality (index.html)
1. **Responsive Image Display**
   - Auto-adjusts to screen size (max 600px width)
   - Fixed height images with object-fit cover
   - Mobile-friendly layout

2. **Navigation System**
   ```javascript
   // Next button handler
   nextBtn.addEventListener('click', () => {
     if (currentIndex < images.length - 1) {
       currentIndex++;
       showSlide(currentIndex);
     } else {
       alert("This is the last slide.");
     }
   });
   ```

3. **Dynamic Content Management**
   - Add new images via URL input
   - Real-time caption updates
   - Automatic slide counter

4. **Playback Controls**
   - Auto-play with 3-second intervals
   - Manual pause/resume
   - Seamless image transitions

## 🛠️ Installation & Setup

1. Create new directory:
   ```bash
   mkdir image-slider
   cd image-slider
   ```

2. Create `index.html` with the provided code
3. Open in web browser:
   ```bash
   python -m http.server  # or use live server
   ```

## 📝 Usage Guide

### 1. Basic Navigation
| Control | Action |
|---------|--------|
| ▶️ Next (❯) | Show next image |
| ◀️ Prev (❮) | Show previous image |
| ⚠️ Boundary | Alert at first/last slide |

### 2. Adding New Images
```javascript
// Add image handler
addBtn.addEventListener('click', () => {
  const newImage = {
    img: "YOUR_URL_HERE",
    caption: "Your Caption"
  };
  images.push(newImage);
});
```

1. Enter valid image URL
2. Add caption text
3. Click "Add Image" button

### 3. Auto-play Controls
| Button | Function |
|--------|----------|
| ▶️ Auto-play | Start 3-second rotation |
| ⏸️ Pause | Stop auto-play |

## 💻 Customization Options

### Modify Default Images
Edit the `images` array in JavaScript:
```javascript
const images = [
  {
    img: "YOUR_IMAGE_URL",
    caption: "Your Caption"
  },
  // Add more images...
];
```

### Adjust Auto-play Timing
```javascript
// Change interval in startAutoplay()
setInterval(() => {
  currentIndex = (currentIndex + 1) % images.length;
  showSlide(currentIndex);
}, 3000); // 3000 = 3 seconds
```

### Style Customization
Edit CSS variables:
```css
.slider-container {
  width: 600px; /* Change max width */
  /* ... */
}

.slider-image {
  height: 400px; /* Change image height */
  /* ... */
}
```
<img width="913" height="814" alt="image" src="https://github.com/user-attachments/assets/c5c5c756-ae2a-4fe8-a07b-3eb19bcd3162" />
## 🖼️ Default Images

1. **Pink City**  
   ![Preview](https://cdn.getyourguide.com/image/format=auto,fit=crop,gravity=auto,quality=60,width=535,height=400,dpr=1/tour_img/2849c5dd4606a53014d5371a9f0feabca062f32c95e0364768498e2b0bfe3ecf.jpg)

2. **Statue of Unity**  
   ![Preview](https://www.indianholidaytrip.com/Upload/Blog/Img_3518_202328241039_SOU_1.jpg)

3. **Misty Forest**  
   ![Preview](https://as1.ftcdn.net/v2/jpg/05/02/48/70/1000_F_502487005_nVDDbjXLEZ2YLNc6UQNqYt19T3MiSsp7.jpg)

4. **Golden Hour Valley**  
   ![Preview](https://miro.medium.com/v2/resize:fit:720/format:webp/1*rPybpXRlwvEIQ4vynbSVeA.jpeg)

## 🔧 Troubleshooting

1. **Images Not Loading**
   - Verify URL validity
   - Check for HTTPS/HTTP mismatches
   - Ensure image hosts allow CORS

2. **Auto-play Not Working**
   - Verify no JavaScript errors
   - Check browser console (F12)
   - Ensure no duplicate IDs

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

Created by [PATEL KUSH] ([kushpatel8543@gmail.com](kushpatel8543@gmail.com))
```

This README includes:
1. Proper indexing showing `index.html` as main file
2. Code snippets from actual implementation
3. Image previews using actual URLs
4. Troubleshooting section
5. Visual tables for controls
6. Detailed customization instructions
7. Actual code examples for modification
8. Proper project structure documentation

The documentation follows the structure shown in your Google Doc while maintaining all functionality from your original HTML/CSS/JS code.


