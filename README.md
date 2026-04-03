 

# 📌  Digital Clock Web App

A simple real-time digital clock built using:

* HTML
* CSS
* JavaScript

It displays the current time and updates every second.

---

# 📄 `index.html`

```html id="clk001"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="clock-container">
        <h1>Digital Clock</h1>
        <div id="clock">00:00:00</div>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

---

# 🎨 `style.css`

```css id="clk002"
body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #1e1e2f;
    font-family: Arial, sans-serif;
    color: white;
}

.clock-container {
    text-align: center;
    padding: 30px;
    border-radius: 15px;
    background: #2c2c3e;
    box-shadow: 0 0 20px rgba(0,0,0,0.5);
}

h1 {
    margin-bottom: 20px;
}

#clock {
    font-size: 50px;
    font-weight: bold;
    letter-spacing: 2px;
}
```

---

# ⚙️ `script.js`

```javascript id="clk003"
function updateClock() {
    const now = new Date();

    let hours = now.getHours();
    let minutes = now.getMinutes();
    let seconds = now.getSeconds();

    hours = hours < 10 ? "0" + hours : hours;
    minutes = minutes < 10 ? "0" + minutes : minutes;
    seconds = seconds < 10 ? "0" + seconds : seconds;

    document.getElementById("clock").innerText =
        `${hours}:${minutes}:${seconds}`;
}

setInterval(updateClock, 1000);
updateClock();
```

---

# 📘 `README.md`

```markdown id="clk004"
# 🕒 Digital Clock Web App

## 📌 Overview
This is a simple **Digital Clock web application** built using HTML, CSS, and JavaScript. It displays the current time and updates every second in real-time.

---

## 🚀 Features
- Live updating digital clock  
- 24-hour format display  
- Clean and modern UI  
- Responsive centered design  

---

## 🛠️ Technologies Used
- HTML5  
- CSS3  
- JavaScript (Vanilla JS)

---

## 📂 Project Structure
```

digital-clock/
│
├── index.html     # Main HTML file
├── style.css      # Styling file
└── script.js      # JavaScript logic

````id="clk005"

---

## ▶️ How to Run

### 1. Download the project
No installation required.

### 2. Open file
Simply open:
```

index.html

````

in any browser (Chrome, Edge, Firefox).

---

## 💡 How It Works

* JavaScript gets current system time using `Date()`
* Time is formatted to HH:MM:SS
* `setInterval()` updates the clock every 1 second

---

## 📈 Future Improvements

* Add AM/PM format
* Add date display
* Add alarm feature
* Add different clock themes (dark/light mode)

---

 
