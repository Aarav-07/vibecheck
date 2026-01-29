window.onblur = null;

window.onfocus = null;

document.onvisibilitychange = null;

document.addEventListener("visibilitychange", function(event) {

event.stopImmediatePropagation(); // Blocks the event from executing

}, true);

window.addEventListener("blur", function(event) {

event.stopImmediatePropagation();

}, true);

window.addEventListener("focus", function(event) {

event.stopImmediatePropagation();

}, true);

Object.defineProperty(document, "hidden", { value: false, configurable: true });

Object.defineProperty(document, "visibilityState", { value: "visible", configurable: true });
document.addEventListener('copy', (e) => e.stopPropagation(), true);

document.addEventListener('paste', (e) => e.stopPropagation(), true);