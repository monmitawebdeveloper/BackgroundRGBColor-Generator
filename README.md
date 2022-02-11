# BackgroundRGBColor-Generator
/* Project Requirement:
 - Change the background color by generating random rbg color by clicking a button */

//  Step-1 - creating onload handler
window.onload = () => {
  main();
};

// Step-2 - random color generator function
function geneateRGBColor() {
  // rgb(0, 0, 0), rgb(255, 255, 255)
  const red = Math.floor(Math.random() * 255);
  const green = Math.floor(Math.random() * 255);
  const blue = Math.floor(Math.random() * 255);

  return `rgb(${red}, ${green}, ${blue})`;
}

// Step-3 - collect all necessary references
function main() {
  const rootEl = document.getElementById("root");
  const btnEl = document.getElementById("change-btn");

  // Step-4 - handle the click event
  btnEl.addEventListener("click", function () {
    const bgColor = geneateRGBColor();
    rootEl.style.backgroundColor = bgColor;
  });
}
