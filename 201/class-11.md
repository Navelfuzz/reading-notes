# Class 11 Readings: Audio, Video, Images

## Video and Audio Content

[Video and Audio Content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)

*Questions*

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.
2. Describe the use of the `src` and `controls` attributes in the `<video>` element.
3. Why is it important to have **fallback content** inside the `<video>` element?
4. Write a very short story where `<audio>` and `<video>` are characters.

*Answers*

1. A major and significant change has been bandwidth and its availability globally. *Back in my day...* dial up was so slow that a site such as
YouTube wouldn't function. Also A/V weren't intregal parts of web structure. Plugins were used to deliver them as a means of compressing data whereas
now this is done in different ways.
2. `src` simply is the URL source of the video file. `controls` displays the default video player controls within the browser.
3. Fallback content makes up for browser compatibility conflicts, plugin availability, and accessibility considerations.
4. One day at show and tell Video made a display of "moving pictures" that are made of a series of discrete images changing from one to the next in rapid succession.
Audio sang a song... which nobody liked, because mumble rap is a regression within its genre and in a capella form sounds like someone having a stroke.

## A Complete Guide to Grid

[A Complete Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

*Questions*

1. How does Grid layout differ from Flex?
2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.

*Answers*

1. Grid layout is 2 dimensional and Flex is one dimensional. Grid is best for both rows and colums and Flex is better when a single axis is needed.
2. A grid container is an HTML element that serves as the parent/container for a grid layout. Item is the elements within the container such as div's article's
or image's. The line is a horizontal or vertical segment of the grid framework.

## Responsive Images

[Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

*Questions*

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
2. Define the following `<img>` attributes `srcset` and `sizes`. Write an example of how they are used.
3. How is `srcset` more helpful for responsive images than CSS or JavaScript?

*Answers*

1. Optimization. Helps pages load faster, optimizes bandwidth usage and therefore improves SEO.
2. `srcset` allows you to specify a set of image sources and their corresponding sizes or resolutions. This helps determine which image to download in order to optimize.
`sizes` specifies the display area in CSS on the page.
3. Its an automatic selection that chooses the most appropriate image and reduces load times from the origin of the image addition being brought forth to the page, not after the 
fact.

### Bookmark and Review

[Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
[Other Embedding Technologies](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies)
