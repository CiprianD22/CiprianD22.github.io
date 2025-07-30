# Ciprian's page

## Latest tips / quick solutions:

* Send HTTP Rest API request using <ins>Windows Powershell Version 7</ins> with Bearer/Token Authentication
```powershell
# The **Invoke-RestMethod** requires an instance of .NET SecureString in which the Bearer Token is to be stored:
$sString = [SecureString]::new()

# Populate the SecureString with our Token string
foreach ($c in "MyTokEnStrinGHexHhHhhHhHh".ToCharArray()) { $sString.AppendChar($c) }

# Invoke the API call using HTTP ('irm' is the abbreviation for **Invoke-RestMethod** in Powershell
$response = irm "https://api.host.com/client/v4/user/tokens/verify" -Authentication Bearer -Token $sString
```

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/CiprianD22/CiprianD22.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
