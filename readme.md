# How to Open the File

Find the file called laundry-landing.html on your computer
Double-click it
It will automatically open in your web browser (Chrome, Firefox, Edge — any of them work)
That's it! No installation needed, no internet required (except for the hero photo which loads from the web)

## What's New in This Project

1. A Hamburger Menu (Mobile Only)
   You know that little ☰ three-line icon you see on mobile websites? That's called a hamburger menu. We added one to the navbar that only shows up when you're on a small screen (like a phone). On a desktop or laptop, it stays completely hidden — the regular nav links show instead.
2. CSS-Only Toggle — No JavaScript
   Normally, making a menu open and close when you click something requires JavaScript (a programming language that handles interactions). We skipped that entirely. Instead, we used a neat pure CSS trick — wrapping the hamburger icon inside a <button> tag and using something called the :focus pseudo-class. When you click the button, the browser puts it "in focus" (like highlighting a text box), and we use that moment in CSS to make the menu slide in. Click away and it disappears. All CSS, zero JavaScript.
3. Responsive Layout
   The page automatically rearranges itself depending on your screen size:
   Desktop → text on the left, laundry room photo on the right, full nav visible
   Mobile → everything stacks vertically, photo goes below text, hamburger menu appears

### The Tricky Part — Hamburger Menu Challenges

1. The Menu Was Showing on Desktop Too
   When we first wrote the :focus rule that shows the menu, it worked on all screen sizes — including desktop. So even on a big screen where the hamburger was invisible, the menu could still technically be triggered.
   Fix: We moved the :focus rule inside the mobile media query (@media max-width: 768px). This means the rule only exists for small screens — on desktop it simply doesn't exist at all.
2. The :focus Trick Has One Limitation
   The CSS :focus trick works well, but it only keeps the menu open as long as the button stays focused. The moment you click somewhere else on the page, the button loses focus and the menu closes. This is actually fine for a simple use case — but worth knowing if you ever want a menu that stays open until you click a close button (that would need JavaScript).
