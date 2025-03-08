

# **Netflix Website Clone - README**

Yeh ek simple **Netflix clone** website hai jo **HTML** aur **CSS** ka use karke banayi gayi hai. Main yaha pe har section ko explain karunga taaki aapko samajh aaye ki yeh code kaise kaam karta hai.

---

### **1. HTML Structure**

#### **Basic Layout**
- **HTML** structure mein website ka basic layout defined hai.
- **Header Section**: Isme **Netflix logo**, main navigation links (jaise **Home**, **TV Shows**, etc.), aur sub-navigation for account-related links (search, bell icon, account) hain.

  ```html
  <header>
    <div class="netflixlogo"> <!-- Netflix logo -->
      <a id="logo" href="#home"><img src="logo.png" alt="logo image"></a>
    </div>
    <nav class="main-nav"> <!-- Main navigation bar -->
      <a href="#Home">Home</a>
      <a href="#TV Shows">TV Shows</a>
      <a href="#Movies">Movies</a>
      <a href="#Originals">Originals</a>
      <a href="#">Recently Added</a>
    </nav>
    <nav class="sub-nav"> <!-- Sub navigation (account, bell, search) -->
      <a href="#"><i class="fas fa-search sub-nav-logo"></i></a>
      <a href="#"><i class="fas fa-bell sub-nav-logo"></i></a>
      <a href="#">Account</a>
    </nav>
  </header>
  ```

#### **Main Sections**
- **Popular on Netflix**: Yeh section popular images ko display karta hai jaise **movies, TV shows**, etc. Yeh images anchor (`<a>`) tags ke through clickable hain.
  
  ```html
  <h1>Popular on Netflix</h1>
  <div class="box">
    <a href=""><img src="p1.png" alt=""></a>
    <a href=""><img src="p2.png" alt=""></a>
    <!-- aur images -->
  </div>
  ```

- **Trending Now, TV Shows, Movies**: Yeh sections similar structure follow karte hain. Inme images aur information dikhayi gayi hai jo **Trending Movies**, **TV Shows**, aur **Netflix Originals** se related hain.

  ```html
  <h1>Trending Now</h1>
  <div class="box">
    <a href=""><img src="t1.png" alt=""></a>
    <!-- aur images -->
  </div>
  ```

#### **Footer Section**
- Yeh section footer ke liye hai. Isme **social media links** (Facebook, Instagram, etc.) aur **legal information** hai Netflix ke baare mein.

  ```html
  <footer>
    <p>&copy 1997-2025 Netflix, Inc.</p>
    <p>Carlos Avila &copy 2025</p>
  </footer>
  ```

---

### **2. CSS Styling**

#### **Root Variables**
- **CSS** mein variables jaise `--primary`, `--light`, aur `--dark` define kiye gaye hain jo website ke colors ko manage karne mein madad karte hain.

  ```css
  :root {
    --primary: #141414;  /* Main background color */
    --light: #F3F3F3;    /* Light text color */
    --dark: #686868;     /* Dark text color */
  }
  ```

#### **General Styling**
- **HTML, Body**: Body ka background dark hai aur text ka color light hai. Yeh poora page 100% width pe set kiya gaya hai.
  
  ```css
  html, body {
    width: 100%;
    min-height: 100vh;
    margin: 0;
    padding: 0;
    background-color: var(--primary);  /* Dark background color */
    color: var(--light);               /* Light text color */
  }
  ```

- **Header Styling**: Header mein **grid layout** ka use kiya gaya hai jisme logo, main navigation, aur sub-navigation properly aligned hain. Yeh layout automatically screen size ke according adjust ho jata hai.

  ```css
  header {
    padding: 20px;
    position: fixed;
    top: 0;
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    background-color: var(--primary);
  }
  ```

#### **Responsive Layout (Media Queries)**
- **Mobile aur Tablet Views**: `@media` queries ka use karke layout ko different screen sizes ke liye adjust kiya gaya hai.
  
  - Agar screen **900px se chhoti** hoti hai (tablet), toh grid layout **6 columns** se **4 columns** mein change ho jata hai.
  - Agar screen **700px se chhoti** hoti hai (mobile), toh layout **1 column** ho jata hai.

  ```css
  @media(max-width: 900px) {
    .box {
      grid-template-columns: repeat(4, minmax(100px, 1fr));
    }
  }

  @media(max-width: 700px) {
    .box {
      grid-template-columns: repeat(1, 1fr);  /* Mobile view mein ek column */
    }
  }
  ```

#### **Hover Effects**
- **Hover effects** apply kiye gaye hain images pe. Jab user kisi image pe hover karta hai, image thodi si **zoom** ho jati hai. Isse interactive effect milta hai.

  ```css
  .box a:hover {
    transform: scale(1.4);  /* Hover pe image enlarge hoti hai */
  }
  ```

#### **Footer aur Social Media Links**
- Footer ko style kiya gaya hai taaki wo neat aur aligned dikhe. Social media icons bhi clickable hain aur unpe hover karne pe unka color change hota hai.

  ```css
  .logos a {
    padding: 10px;
  }

  .logos {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: repeat(2, 1fr);
    text-align: center;
  }
  ```

---

### **3. Key Notes for Beginners**
- **HTML Structure**: Yeh website ka skeleton hai. Isme header, main content, aur footer sections defined hain.
- **CSS Styling**: Yeh website ke looks define karta hai (colors, layout, images, etc.).
- **Media Queries**: Yeh feature website ko responsive banata hai. Matlab, screen size ke hisaab se layout change hota hai (mobile vs. desktop).
- **Hover Effects**: Jab user image pe hover karta hai, toh image thodi badi ho jati hai, jo ek interactive effect deta hai.

---

### **Conclusion**

Yeh **Netflix Clone** project ek simple example hai ki kaise **HTML** aur **CSS** ka use karke ek **responsive** aur **interactive** website banayi ja sakti hai. Aap ise apne hisaab se customize kar sakte hain jab aap aur advanced web development sikhenge.

---

