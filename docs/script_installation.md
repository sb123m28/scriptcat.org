# 脚本安装
// ==UserScript==
// @name Auto Dark Mode
// @namespace http://scriptcat.org
// @version 1.0
// @description Automatically enable dark mode on websites
// @author ScriptCat User
// @match *://*/*
// ==/UserScript==

function enableDarkMode() {
const css = `body { background-color: #121212; color: #e0e0e0; }`;
const style = document.createElement('style');
style.textContent = css;
document.head.appendChild(style);
console.log('🐱 ScriptCat: Dark mode enabled');
}

function isDarkModePreferred() {
return window.matchMedia('(prefers-color-scheme: dark)').matches;
}

if (isDarkModePreferred()) {
enableDarkMode();
}
