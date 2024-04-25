## Flask Application Design

### Problem: Convert one provided PDF scientific publication into smaller snippets for easier consumption, to enhance readability for the user.

### Flask Application Structure

#### HTML Files:

1. **index.html**: The main landing page of the application. It will include a form that allows the user to upload a PDF file.
2. **results.html**: The page that displays the converted PDF snippets. It will have a list of snippets, each with its own title, abstract, and link to the full text.

#### Routes:

1. **root**: The route for the main landing page. It will render the `index.html` file.
2. **upload**: The route that handles the file upload and conversion. It will take the uploaded PDF, split it into snippets, and store them in a database. It will then redirect the user to the results page.
3. **results**: The route that displays the converted PDF snippets. It will query the database and retrieve the stored snippets, then render the `results.html` file with the retrieved data.