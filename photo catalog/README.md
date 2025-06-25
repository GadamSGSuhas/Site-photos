# Photo Catalog

A minimalist photo catalog showcasing different photography categories with example images.

## Contents

- Main page with 6 photography categories
- Individual category pages with 6 example photos each:
  - Landscapes
  - Portraits
  - Wildlife
  - Architecture
  - Macro
  - Black & White

## How to Use on Another Computer

### Option 1: Using the ZIP file

1. Transfer the `photo_catalog.zip` file to the target computer
2. Extract the ZIP file to a location of your choice
3. Open the extracted folder and double-click on `index.html` to view the catalog in your web browser

### Option 2: Manual Transfer

1. Copy the entire "photo catalog" folder to a USB drive or cloud storage
2. Transfer the folder to the target computer
3. Open the folder and double-click on `index.html` to view the catalog in your web browser

## Publishing as a Website

### Option 1: GitHub Pages (Free)

1. Create a GitHub account if you don't have one already
2. Create a new repository (e.g., "photo-catalog")
3. Upload the contents of the "photo catalog" folder to your repository
   - You can do this by dragging and dropping files in the GitHub web interface
   - Or by using Git commands if you're familiar with them
4. Go to repository Settings > Pages
5. Under "Source", select "main" branch and the root folder
6. Click "Save"
7. Your website will be published at `https://yourusername.github.io/photo-catalog/`

### Option 2: Netlify (Free)

1. Create a Netlify account at [netlify.com](https://www.netlify.com/)
2. Click "Add new site" > "Import an existing project"
3. Connect to your GitHub/GitLab/Bitbucket account or drag and drop the "photo catalog" folder
4. Your site will be deployed with a random subdomain (e.g., `https://random-name-123456.netlify.app`)
5. You can set up a custom domain in the Netlify settings if desired

### Option 3: Traditional Web Hosting

1. Sign up for a web hosting service (e.g., Bluehost, HostGator, DreamHost)
2. Access your hosting control panel (usually cPanel)
3. Use the File Manager or FTP client (like FileZilla) to upload the contents of the "photo catalog" folder
4. Upload to the public_html or www directory of your hosting account
5. Your website will be accessible at your domain name

### Option 4: Cloud Storage Services

#### Amazon S3:
1. Create an AWS account and navigate to S3
2. Create a new bucket with a unique name
3. Upload the contents of the "photo catalog" folder to the bucket
4. Under "Properties", enable "Static website hosting"
5. Set "index.html" as the index document
6. Make the bucket public by adjusting the bucket policy
7. Your website will be available at the S3 endpoint URL

#### Google Cloud Storage:
1. Create a Google Cloud account and navigate to Cloud Storage
2. Create a new bucket and upload the contents of the "photo catalog" folder
3. Make the bucket public and enable website configuration
4. Set "index.html" as the main page
5. Your website will be available at the GCS endpoint URL

## Notes

- This is a static HTML website that doesn't require any server or installation
- All photos are loaded from Unsplash URLs, so an internet connection is required to view the images
- The website is responsive and will work on different screen sizes
- Compatible with all modern web browsers (Chrome, Firefox, Safari, Edge)

## Customization

### Adding Your Own Photos

#### Option 1: Using External Image URLs

1. Open the category HTML file you want to modify (e.g., `photo catalog/categories/landscapes/index.html`)
2. Find the image section in the HTML code:
   ```html
   <div class="photo-item">
       <img src="https://images.unsplash.com/photo-..." alt="Photo Title" class="photo-image">
       <div class="photo-info">
           <h2 class="photo-title">Photo Title</h2>
           <div class="photo-meta">
               <span>Location</span>
               <span>Photo by Photographer</span>
           </div>
       </div>
   </div>
   ```
3. Replace the `src` attribute with your own image URL
4. Update the `alt` text, title, and metadata as needed

#### Option 2: Using Local Images

1. Create category folders inside the `images` directory:
   ```
   photo catalog/
   ├── images/
   │   ├── landscapes/
   │   ├── portraits/
   │   ├── wildlife/
   │   ├── architecture/
   │   ├── macro/
   │   └── black-and-white/
   ```

2. Add your images to the appropriate category folder

3. Update the HTML files to reference your local images:
   ```html
   <!-- Change this -->
   <img src="https://images.unsplash.com/photo-..." alt="Photo Title" class="photo-image">
   
   <!-- To this -->
   <img src="../../images/landscapes/your-image.jpg" alt="Photo Title" class="photo-image">
   ```

### Adding More Photos to a Category

To add additional photos to a category:

1. Open the category HTML file (e.g., `photo catalog/categories/landscapes/index.html`)
2. Find the `<section class="photo-grid">` element
3. Add a new photo item by copying and pasting this template:
   ```html
   <div class="photo-item">
       <img src="../../images/category-name/your-image.jpg" alt="Photo Title" class="photo-image">
       <div class="photo-info">
           <h2 class="photo-title">Photo Title</h2>
           <div class="photo-meta">
               <span>Location or Description</span>
               <span>Photo by Photographer</span>
           </div>
       </div>
   </div>
   ```
4. Update the image path, title, and metadata as needed
5. Update the photo count on the main page (`photo catalog/index.html`) to reflect the new total

### Creating a New Category

1. Create a new folder in the `categories` directory (e.g., `photo catalog/categories/new-category/`)
2. Create an `index.html` file in the new category folder (copy from an existing category and modify)
3. Create a corresponding folder in the `images` directory if using local images
4. Add the new category to the main page (`photo catalog/index.html`) by copying an existing category card and updating it

## Credits

- All example photos are from [Unsplash](https://unsplash.com/)
- Design and code created with minimalist principles
