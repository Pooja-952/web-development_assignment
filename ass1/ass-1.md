
Q.1 is it a tag of html? If not, what is it and why do we use it?
//Solution---> // The declaration instructs the browser on how to interpret and display the HTML code. Its main function is to inform the browser that the document conforms to HTML5, The primary role of the doctype declaration is to ensure that the browser renders the document in standards mode. Using is considered a best practice and is the recommended declaration for HTML5 documents. It guarantees that the document is treated as an HTML5 document and that the browser follows the HTML5 specifications for displaying the content.

// Q.2 Explain Semantic tags in html? And why do we need it?
// Solution---> // Semantic tags in HTML serve the purpose of providing meaning and context to the content they enclose. They enhance readability and comprehension of the HTML code by organizing it into distinct sections. // Example of semantic tags :-

, , , , , . // Semantic tags are needed as they enhance the structure, accessibility, search engine visibility, consistency, and maintainability of web pages, making them an integral part of modern HTML development.

// Q.3 Differentiate between HTML Tags and Elements?
//Solution---> // HTML Tags: // HTML tags serve as the markup elements that define the structure and semantics of an HTML document. They are enclosed within angle brackets (< >,</>) and consist of the tag name, such as

, , ,

, , etc. These tags are used to mark the beginning and end of an element. // HTML Elements: // HTML elements include the HTML tag, its associated attributes, and the content within it. An HTML element is formed by the combination of the opening tag, optional content, and the closing tag. It represents a specific part or component within an HTML document. For instance, in the element

Hello world , the tag "h6" forms the element, and the angle brackets serve as the tags enclosing the element. The tags hold the elements, and the elements hold the data.

// Q.8 What is the difference between
tag and

tag? // Solution--->

The tag is an HTML element used to insert images into a web page. It is a self-closing tag and doesn't require a closing tag. The tag is used to specify the image source, alt text for accessibility, and additional attributes like width and height. It represents a single image in the document. On the other hand, the

tag serves the purpose of grouping self-contained content blocks, such as images or multimedia objects, along with their respective captions. It provides a semantic structure for the content, making it easier to style and ensure accessibility. The tag is often used alongside the tag, which provides the caption for the enclosed content. The difference between

tag and the tag is that the

tag is used specifically for inserting standalone images, whereas the tag is used to group an image or multimedia object together with its caption.

// Q.9 What’s the difference between html tag and attribute and give example of some global attributes?
// Solution--->

HTML Tags: HTML tags serve as the markup elements utilized to establish the structure and meaning of an HTML document. These tags are enclosed within angle brackets (< >) and consist of the tag name, such as ,

, , ,

, , and more. HTML tags play a crucial role in indicating the initiation and conclusion of an element or representing stand-alone elements. HTML Attributes: On the other hand, HTML attributes are employed within HTML tags to provide supplementary information or configure elements. These attributes are specific to certain HTML tags and modify their behavior, appearance, or functionality. Attributes are specified in the format of key-value pairs within the opening tag of an element, utilizing the attributeName="value" structure. Some examples of attributes include src, href, class, id, alt, style.

Global Attributes: Global attributes are attributes that can be used with any HTML tag regardless of its specific purpose or meaning. Some examples of global attributes include:

class: Specifies one or more CSS class names to apply to an element for styling. id: Provides a unique identifier for an element, allowing it to be targeted by CSS. style: Allows inline styling of an element by specifying CSS rules directly.

 