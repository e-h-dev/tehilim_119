# tehilim_119

## About this Project
When reciting Tehillim on behalf of someone in need, it is customary to conclude with the verses of Perek 119. This chapter is structured around the Hebrew Aleph-Beis, with each letter introducing a set of verses. A meaningful tradition involves spelling out the individual's name—along with their mother's name—by reciting the verses corresponding to each letter, often followed by a short prayer such as קרע שטן.

Traditionally, this process requires the reciter to manually locate each letter's section in the Tehillim, flipping back and forth through pages. In group settings, a leader may call out each letter, guiding the participants through the recital. While some have streamlined the process by copying and pasting relevant verses from digital sources, this often places a heavy burden on the organizer.

This project offers a simple, elegant solution: a web app that displays the full text of Perek 119 and allows users to input a name. The app then automatically generates the exact verses in the correct order, ready for recital. It also includes a download option for printing hard copies, making it ideal for both personal and communal use.

By reducing preparation time and eliminating page-turning, this tool enhances focus, kavana, and ease—bringing clarity and dignity to a cherished tradition.


## Bugs
1. During testing of the function designed to clear the main Tehilim text, an unexpected issue occurred: the margins were also removed, and the grey background color disappeared. This resulted in a visually unbalanced and unusual appearance in the main window.

I resolved the issue by inspecting the layout in DevTools. After a moment, I realized that the Bootstrap row containing the Tehilim text was only sized according to its content. Since the function clears the text by setting its CSS to display: none, the column effectively became empty and lost its height. This caused the page to render awkwardly, ending abruptly halfway down and creating an obscure visual effect. To fix this, I added a height: 100vh style to the div containing the text, ensuring that the section maintains its height even after the content is hidden.
