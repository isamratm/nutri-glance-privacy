from pathlib import Path

# Define the content of the privacy policy in markdown format
privacy_policy_markdown = """
# Privacy Policy for Nutri Glance

_Last updated: June 5, 2025_

Nutri Glance (“we,” “our,” or “us”) is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application.

## 1. Information We Collect

- **Photos**: When you use the scan feature, you provide a photo of food, which is sent to our server (via OpenAI's ChatGPT API) for nutritional analysis.
- **Usage Data**: We may collect anonymized app usage statistics for the purpose of improving app performance and user experience.

We do **not** collect or store any personal data like your name, email address, or location.

## 2. How We Use Your Information

- To analyze food photos using AI and provide nutritional insights.
- To improve our services through anonymized usage analytics.

## 3. Data Handling

- Your food image is sent to OpenAI’s ChatGPT API for analysis.
- We do **not** store or retain any images or responses on our servers.
- No personally identifiable information is collected, stored, or shared.

## 4. Sharing Your Information

We do **not** share your personal data with third parties. However, image analysis is done through OpenAI API, and is subject to OpenAI’s own privacy and usage terms.

## 5. Your Rights

As we do not collect any personal or persistent data, we cannot provide, correct, or delete data on request. No identifiable user data is stored or accessible.

## 6. Security

We use secure protocols to transmit your images for analysis and do not store any data on our servers.

## 7. Children’s Privacy

Nutri Glance does not knowingly collect any information from children under the age of 13. The app is not intended for use by children under 13 without parental guidance.

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Any changes will be posted on this page with an updated date.

## 9. Contact Us

If you have any questions or concerns, please contact us at:  
📧 support@nutriglance.app
"""

# Create the HTML file content for GitHub Pages
html_content = f"""
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy | Nutri Glance</title>
    <style>
        body {{ font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; margin: 40px; line-height: 1.6; }}
        h1, h2 {{ color: #2e7d32; }}
        pre, code {{ background: #f4f4f4; padding: 4px; border-radius: 4px; }}
    </style>
</head>
<body>
{privacy_policy_markdown.replace('\n', '<br>')}
</body>
</html>
"""

# Save the file for GitHub Pages
output_file = Path("/mnt/data/privacy_policy.html")
output_file.write_text(html_content)

output_file.name
