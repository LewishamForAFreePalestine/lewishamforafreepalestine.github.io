# Contact MP Template

This template allows you to create a customizable tool for contacting MPs with any message or campaign. Users can easily copy this template and customize it for their specific needs.

You can open a pull request to this repository to host under https://lewishamforafreepalestine.github.io/ or copy the files into your own web hosting.

## How to Use This Template

1. **Copy the directory**: Copy the entire `templates/contact-mp/` directory to the `docs/` folder with your campaign name (e.g., `docs/your-campaign-name/`)
2. **Customize the email content**: Edit the `body.txt` file to contain your specific message
3. **Customize the page**: (Optional) Edit `index.html` to update the page title, heading, or styling
4. **Test locally**: Test your campaign by serving the files through a local web server (e.g. `python3 -m http.server 8080 -d templates/contact-mp/` then opening [http://localhost:8080](http://localhost:8080))
5. **Submit for deployment**: Once everything is ready, open a pull request to deploy your campaign to GitHub Pages

## Email Template Tokens

The email body in `body.txt` can use the following tokens that will be automatically replaced with user input:

- `{mpName}` - The MP's name
- `{constituency}` - The MP's constituency
- `{signee}` - User's first and last name combined
- `{streetAddress}` - User's street address
- `{city}` - User's city
- `{postcode}` - User's postcode
- `{phoneNumber}` - User's phone number

## Example Usage

To create a campaign about environmental issues, you would:

1. Copy this directory to a new location in the docs directory (e.g., `docs/campaigns/environment-action/`)
2. Edit `body.txt` to contain your environmental message using the tokens above
3. Optionally edit the `<h1>` tag in `index.html` to say "Tell your MPs about Climate Action"
4. Host the files on a web server

## Technical Requirements

- The template uses jQuery (loaded from CDN)
- Must be served via HTTP/HTTPS (not file://) due to fetch() security restrictions
- Uses the UK Parliament Members API to find MP contact information