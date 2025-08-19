# Seen Instagram Stories Anonymously 🕵️‍♂️

**Seen Instagram Stories Anonymously** is a Chrome extension that allows you to view Instagram stories without notifying the user. You can toggle the extension ON/OFF from the browser toolbar.  

---

## ✨ Features
- View Instagram stories without sending "seen" notifications.  
- Easy toggle via Chrome browser toolbar.  
- Badge indicator shows **Active** (extension is blocking story seen requests) or **OFF**.  
- Lightweight and simple to use.  

---

## 🛠️ Installation
1. Clone or download the repository.  
2. Open Chrome and navigate to `chrome://extensions/`.  
3. Enable **Developer mode** (top-right toggle).  
4. Click **Load unpacked** and select the folder containing `manifest.json` and `background.js`.  
5. The extension icon will appear in your Chrome toolbar.  

---

## 🚀 Usage
- Click the extension icon in the toolbar to toggle **Active/OFF** mode.  
- When **Active**, the extension blocks requests that would mark Instagram stories as "seen".  
- The badge color indicates the current state:  
  - **Blue (#0097ff)** → Active  
  - **Gray (#777)** → OFF  

---

## ⚡ How It Works
1. Listens to outgoing Instagram story requests via `chrome.webRequest.onBeforeRequest`.  
2. Cancels requests to `https://*.instagram.com/api/v1/stories/reel/seen*` when **Active**.  
3. Updates the badge text and color based on the toggle state.  

---

## 📂 Files
```
background.js        # Main logic for blocking Instagram story seen requests
manifest.json        # Chrome extension manifest file
icon.png             # Extension icon
```

---

## 📝 Notes
- Works only in Chrome.  
- Make sure to allow permissions when installing the extension.  
- Can be toggled on/off at any time without restarting Chrome.  
