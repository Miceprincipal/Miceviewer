# Miceviewer
A tragically simple but lightweight side by side .PNG and .JSON viewer for NFT artists to both check and more easily showcase work to clients.

Just a painfully simple little html-based side by side viewer that can be dropped painlessly into the root folder of any nft compiler that uses a build folder with image and json output folders.
There is also a version to be dropped straight inside build folders with zero editing to make life easier for showing clients work. 

It has a 3 speed slideshow option with 2,3 and 5 second options as well as regular next and previous options.

As it stands its setup to handle 10000 images starting at 0.png. 

If need be alter the following line to required numbers:

let currentImageIndex = 0;
        const totalImages = 10000;


If you wish to adjust the slideshow timings 

        auto2sButton.addEventListener('click', () => {
            autoAdvance(2000);
        });

        auto3sButton.addEventListener('click', () => {
            autoAdvance(3000);
        });

        auto5sButton.addEventListener('click', () => {
            autoAdvance(5000);
        });

just alter the timings in thousandths of a second and then

   const auto2sButton = document.getElementById('auto-2s-button');
        const auto3sButton = document.getElementById('auto-3s-button');
        const auto5sButton = document.getElementById('auto-5s-button');

relabel buttons as needed.

Image and json folder locations are here. 

        function loadAndDisplayImage(index) {
            currentImage.src = `images/${index}.png`;
            jsonIframe.src = `json/${index}.json`;

It's... basic.

But hopefully it's helpful to someone as it's something that would have been handy for me before.
