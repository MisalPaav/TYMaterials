# Web Development CAE 3 Question Bank

- [Web Development CAE 3 Question Bank](#web-development-cae-3-question-bank)
  - [Answers](#answers)

## Answers

## **1\. Comparison between Domain Names and Web Hosting**

| Aspect | Domain Name | Web Hosting |
| --- | --- | --- |
| Definition | A domain name is the web address used to identify a website on the internet. For example, "example.com." | Web hosting refers to the service that provides server space and resources to store website files and make them accessible on the internet. |
| Function | Acts as the address that users type in their browser to access a website. | Stores website files, databases, and applications and delivers them to users when they access the corresponding domain. |
| Ownership | Purchased and renewed through domain registrars. | Provided by web hosting companies on a subscription basis. |
| Types | Can include top-level domains (TLDs) like .com, .org, or country-code TLDs like .uk, .de. | Various types of hosting options, including shared hosting, VPS hosting, dedicated hosting, and cloud hosting. |
| Pricing | Paid annually or for multiple years, pricing varies depending on the domain and registrar. | Subscription-based, with pricing based on the type of hosting and resources allocated. |
| Customization | Can be customized to point to different hosting servers or services. | Allows customization of server configurations, software, and resources based on the hosting plan. |
| Examples | "google.com," "wikipedia.org" | Bluehost, HostGator, AWS, DigitalOcean |

## **2\. Types of Web Hosting**

There are several types of web hosting, each with its own features and benefits:

- **Shared Hosting:** Multiple websites share the same server and its resources. It's cost-effective but may have limited resources.

- **Virtual Private Server (VPS) Hosting:** A virtualized server with dedicated resources for each website. It offers more control and scalability.

- **Dedicated Hosting:** Entire server dedicated to one website. It provides maximum control and performance but is more expensive.

- **Cloud Hosting:** Websites are hosted on a network of virtual servers, offering scalability and reliability. Users pay for what they use.

- **WordPress Hosting:** Specialized hosting optimized for WordPress websites, including automatic updates and security features.

- **E-commerce Hosting:** Tailored for online stores with features like SSL certificates and e-commerce platforms.

- **Reseller Hosting:** Users can resell hosting services to others, typically with white-label options.

## **3\. Design & Implement Popup Boxes in JavaScript**

Here's an example of how to create different types of popup boxes using JavaScript:

- **Alert Box:**

javascript

`alert("This is an alert box!");`

- **Confirm Box:**

javascript

`if (confirm("Do you want to proceed?")) {     // User clicked OK } else {     // User clicked Cancel }`

- **Prompt Box:**

javascript

`const name = prompt("Please enter your name:", "John Doe"); if (name !== null) {     alert("Hello, " + name + "!"); }`

## **4\. Display Current Date Using JavaScript**

You can display the current date using JavaScript as follows:

javascript

`const currentDate = new Date(); const formattedDate = currentDate.toDateString(); // Format the date as you prefer console.log("Current date: " + formattedDate);`

## **5\. Role of DNS in Web Hosting and Example of Web Publishing Platform**

DNS (Domain Name System) plays a crucial role in web hosting by translating human-readable domain names into IP addresses, allowing users to access websites. DNS servers store DNS records, including A records, which link domain names to IP addresses.

Example of a Web Publishing Platform: WordPress

WordPress is a popular web publishing platform that allows users to create and manage websites. Users can choose a domain name (e.g., mywebsite.com) and a web hosting service, and then install WordPress to create and publish content. DNS records are configured to point the domain to the hosting server's IP address, enabling visitors to access the WordPress site using the chosen domain.

## **6\. Design a table with three rows and four columns containing student details:**

Here's a simple example of an HTML table with three rows and four columns for displaying student details:

html

`<table>   <tr>     <th>Student ID</th>     <th>Name</th>     <th>Age</th>     <th>Grade</th>   </tr>   <tr>     <td>1</td>     <td>John Smith</td>     <td>18</td>     <td>A</td>   </tr>   <tr>     <td>2</td>     <td>Jane Doe</td>     <td>19</td>     <td>B</td>   </tr>   <tr>     <td>3</td>     <td>Mike Johnson</td>     <td>20</td>     <td>C</td>   </tr> </table>`

## **7\. Write a tag to display a list of items (student details):**

You can use an unordered list (ul) or ordered list (ol) element to display a list of items. Here's an example using an unordered list:

```html
<ul>
  <li>Student ID: 1</li>
  <li>Name: John Smith</li>
  <li>Age: 18</li>
  <li>Grade: A</li>
</ul>
```

## **8\. Explain the role of CSS in applying style:**

CSS (Cascading Style Sheets) is used to apply styles and formatting to HTML elements on a web page. Its role includes:

- Changing the colors, fonts, and sizes of text.
- Setting the background colors and images for elements.
- Adjusting the spacing and layout of elements.
- Defining transitions and animations for interactive elements.
- Making the page responsive to different screen sizes.
- Enhancing the visual appeal and user experience of a website.

CSS separates the structure (HTML) and presentation (styles) of a web page, allowing for easy maintenance and consistent design.

## **9\. Why JavaScript is a cross-platform language:**

JavaScript is a cross-platform language because it can be executed in web browsers on various operating systems, such as Windows, macOS, and Linux. It's not tied to any specific platform or OS, making it highly versatile. Additionally, JavaScript can also be used on the server-side (Node.js), which extends its cross-platform capabilities to server applications.

## **10\. Required factors of web hosting:**

Several factors are essential for web hosting:

- **Server Hardware:** Powerful and reliable server hardware to ensure performance and uptime.

- **Server Software:** Appropriate server software, like a web server (e.g., Apache, Nginx), database server, and operating system.

- **Bandwidth and Data Transfer:** Adequate bandwidth to handle website traffic and data transfer limitations defined by the hosting plan.

- **Storage Space:** Sufficient storage for website files, databases, and resources.

- **Security:** Strong security measures, including firewalls, SSL certificates, and regular updates.

- **Backup and Recovery:** Regular data backups and disaster recovery plans.

- **Technical Support:** Reliable customer support to address issues and provide assistance.

- **Scalability:** The ability to scale resources (CPU, RAM, storage) as the website grows.

- **Domain and DNS Management:** Support for domain registration and DNS configuration.

- **Uptime Guarantee:** An uptime guarantee to ensure the website is accessible to users.

- **Cost and Pricing Model:** Clear pricing and payment structure based on the hosting type (shared, VPS, dedicated, cloud, etc.).

- **Control Panel:** An easy-to-use control panel for managing the hosting environment.

The choice of web hosting depends on the specific needs and requirements of a website or application.
## 11. HTML code for Unordered List
html

`<!DOCTYPE html> <html> <head>     <title>Unordered List Example</title> </head> <body>     <h1>Types of Fruits</h1>     <ul>         <li>Apples</li>         <li>Bananas</li>         <li>Oranges</li>         <li>Grapes</li>     </ul> </body> </html>`

In this example, we have an `<ul>` (unordered list) containing several list items (`<li>`), which creates a simple list of fruits.

## 12. Now, let's explain the types of lists, types of hyperlinks, and types of table tags in HTML

**Types of Lists:**

1. **Ordered List (`<ol>`):** An ordered list is a list where each item is numbered or lettered. It is created using the `<ol>` element and contains `<li>` elements for list items.

html

`<ol>   <li>Item 1</li>   <li>Item 2</li>   <li>Item 3</li> </ol>`

2. **Unordered List (`<ul>`):** An unordered list is a list where each item is preceded by a bullet point. It is created using the `<ul>` element and contains `<li>` elements for list items.

html

`<ul>   <li>Item A</li>   <li>Item B</li>   <li>Item C</li> </ul>`

3. **Definition List (`<dl>`):** A definition list is used to define terms and their corresponding definitions. It consists of `<dt>` (term) and `<dd>` (definition) elements.

html

`<dl>   <dt>Term 1</dt>   <dd>Definition of Term 1</dd>   <dt>Term 2</dt>   <dd>Definition of Term 2</dd> </dl>`

**Types of Hyperlinks:**

1. **Standard Hyperlink (`<a>`):** The most common type of hyperlink used for linking to other web pages or resources.

html

`<a href="https://www.example.com">Visit Example</a>`

2. **Email Hyperlink (`<a>` with `mailto:`):** Used to create links that open the user's default email client to send an email.

html

`<a href="mailto:info@example.com">Email Us</a>`

3. **Anchor Hyperlink (`<a>` with `#`):** Links within the same page that scroll to specific sections or elements.

html

`<a href="#section2">Go to Section 2</a>`

4. **File Download Hyperlink:** Links to download files like PDFs, images, or documents.

html

`<a href="myfile.pdf" download>Download PDF</a>`

**Types of Table Tags:**

HTML tables can be created using the following tags:

1. **`<table>`:** The container for the entire table.

2. **`<tr>`:** Defines a table row. It contains one or more table cells (`<td>` or `<th>`).

3. **`<td>`:** Defines a standard table cell. It contains data or content.

4. **`<th>`:** Defines a table header cell. It is typically used in the first row and provides column headers.

5. **`<caption>`:** Optional element to provide a caption or title for the table.

6. **`<colgroup>` and `<col>`:** Used to group and format columns in a table.

7. **`<thead>`, `<tbody>`, and `<tfoot>`:** Group rows into header, body, and footer sections for better table structure.

html

`<table>   <caption>Monthly Sales</caption>   <thead>     <tr>       <th>Month</th>       <th>Sales</th>     </tr>   </thead>   <tbody>     <tr>       <td>January</td>       <td>$5,000</td>     </tr>     <tr>       <td>February</td>       <td>$6,200</td>     </tr>   </tbody>   <tfoot>     <tr>       <td>Total</td>       <td>$11,200</td>     </tr>   </tfoot> </table>`

These are the basic elements and attributes used to create various types of lists, hyperlinks, and tables in HTML.
## 13. HTML tag for Login Page
html

`<!DOCTYPE html> <html> <head>     <title>Login Page</title>     <link rel="stylesheet" type="text/css" href="styles.css"> </head> <body>     <div class="login-container">         <h2>Login</h2>         <form action="login.php" method="post">             <label for="username">Username:</label>             <input type="text" id="username" name="username" required>             <label for="password">Password:</label>             <input type="password" id="password" name="password" required>             <input type="submit" value="Login">         </form>     </div> </body> </html>`

In the example above, we have a basic login page with a form that collects the username and password from the user. The form action points to a hypothetical `login.php` script, which would typically handle the login process on the server-side.

## 14. Advantages of CSS on HTML

1. **Separation of Concerns:** CSS allows separation between the structure (HTML) and presentation (styling) of a web page, making it easier to manage and maintain.

2. **Consistency:** CSS enables consistent styling across an entire website. You can define styles in one place and apply them to multiple elements.

3. **Reusability:** You can reuse CSS styles across multiple pages, reducing the need for redundant code.

4. **Faster Page Loading:** By reducing the size of HTML documents (which includes removing inline styles), web pages can load more quickly.

5. **Responsive Design:** CSS is crucial for creating responsive web designs that adapt to different screen sizes and devices.

6. **Improved Accessibility:** CSS can be used to enhance the accessibility of web content by controlling fonts, colors, and layouts for better readability.

7. **Flexibility:** With CSS, you have fine-grained control over elements, allowing for creative and dynamic designs.

## 15. The Best Type of Web Hosting

The choice of the best web hosting type depends on your specific needs:

1. **Shared Hosting:** Suitable for small websites and beginners. It's cost-effective but may have limited resources due to sharing a server with others.

2. **VPS Hosting:** Offers dedicated resources within a virtual environment. Good for growing websites with moderate traffic.

3. **Dedicated Hosting:** Provides an entire physical server for your website. Ideal for large websites and applications with high traffic.

4. **Cloud Hosting:** Scalable, reliable, and cost-effective. Resources can be adjusted as needed. Examples include AWS, Google Cloud, and Microsoft Azure.

5. **Managed WordPress Hosting:** Optimized for WordPress websites, with automatic updates and enhanced security.

6. **E-commerce Hosting:** Tailored for online stores, with e-commerce features and SSL certificates.

7. **Reseller Hosting:** For users who want to resell hosting services to others.

## 16. Difference between HTML and CSS in Table Format

| Aspect | HTML (Hypertext Markup Language) | CSS (Cascading Style Sheets) |
| --- | --- | --- |
| Purpose | Defines the structure and content of web pages. | Defines the presentation and style of web pages. |
| Role | Content markup, hierarchy, and semantics. | Styling, layout, and design. |
| Tags | Uses tags to define headings, paragraphs, links, etc. | Uses selectors to target HTML elements and apply styles. |
| Formatting | Limited formatting options. | Rich formatting and styling capabilities. |
| Separation of Concerns | Focuses on content. | Focuses on presentation. |
| File Extensions | .html, .htm | .css |
| Example | `<p>This is a paragraph.</p>` | `p { color: blue; font-size: 16px; }` |

## 17. Real-time Applications of CSS

1. **Web Design:** CSS is extensively used to create visually appealing and responsive web designs.

2. **Mobile App Development:** CSS can be used to style mobile apps built with HTML and CSS frameworks like Ionic or PhoneGap.

3. **Print Media:** CSS is used for generating printer-friendly versions of web content.

4. **Interactive Games:** CSS animations and transitions are employed to create simple interactive games within web browsers.

5. **Responsive Emails:** CSS is used to design responsive email templates for marketing and communication.

6. **User Interface (UI) Design:** CSS is crucial for designing the user interface of web applications and software.

7. **E-books:** CSS is used to format and style e-books for digital publication.

8. **Data Visualization:** CSS can enhance the presentation of data through charts, graphs, and visualizations.

CSS plays a vital role in the look and feel of web content and is integral to the web development process.
