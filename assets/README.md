# Assets Directory

This directory contains all reference materials, images, documents, and other resources used throughout the prompt engineering knowledge base.

## Directory Structure

```
assets/
├── images/                    # Image references and examples
│   ├── minimalist-illustrations/   # Minimalist conceptual illustration examples
│   ├── diagrams/                   # Technical diagrams and flowcharts
│   ├── screenshots/                # Screenshot examples
│   └── style-references/           # Visual style guides and references
├── documents/                 # PDF documents, papers, and research materials
├── videos/                    # Video resources and tutorials
├── templates/                 # Downloadable template files
└── references/                # Other reference materials

```

## Organization Guidelines

### Images
- Use descriptive file names (e.g., `cot-example-01.png`, `few-shot-pattern.jpg`)
- Group by category or technique
- Include both successful and unsuccessful examples
- Add metadata or descriptions in accompanying `.md` files when needed

### Documents
- Store research papers, whitepapers, and PDF resources
- Use clear naming conventions with date/version if applicable
- Create index files to list and describe contents

### Videos
- Link to external videos or store local recordings
- Include transcripts or summaries when possible
- Note the date and relevance of content

### Templates
- Store reusable template files (prompts, checklists, frameworks)
- Version templates appropriately
- Include usage instructions

### References
- Miscellaneous reference materials
- Code snippets and examples
- External resource links
- Citation information

## Usage

Reference assets in documentation using relative paths:

```markdown
![Example Image](../assets/images/category/example.png)
[Document Reference](../assets/documents/paper.pdf)
```

## Best Practices

- Keep file sizes reasonable (compress images when possible)
- Use web-friendly formats (PNG, JPG, SVG for images)
- Document the source and usage rights for external materials
- Update the index when adding new categories
- Clean up unused or outdated resources periodically
- Create subdirectories as needed for better organization
