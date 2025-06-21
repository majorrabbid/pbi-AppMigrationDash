# App Migration Dashboard - Power BI Project

## Project Overview
This repository contains DAX queries, visual documentation, and related resources for the App Migration Dashboard Power BI project.

## Structure
pbi-AppMigrationDash/
├── dax-queries/           # DAX measure and calculated column definitions
│   ├── measures/          # Migration metrics and KPIs
│   ├── calculated-columns/# App categorization and status columns
│   └── table-expressions/ # Migration analysis expressions
├── visuals-documentation/ # Screenshots and documentation of dashboard visuals
│   ├── dashboards/        # Main dashboard screenshots
│   ├── reports/           # Migration report documentation
│   └── charts/            # Individual migration chart documentation
├── datasets/              # Migration dataset schemas and relationships
├── reports/               # Migration report metadata and descriptions
└── templates/             # Reusable migration dashboard patterns

## DAX Query Categories

### Measures
- Migration progress metrics
- App completion rates
- Timeline calculations
- Risk assessment indicators

### Calculated Columns
- Migration status categorization
- App priority classifications
- Timeline calculations
- Risk level assignments

## Usage Guidelines

1. **DAX Queries**: Save with descriptive names and include comments
2. **Documentation**: Include screenshots with explanations
3. **Naming Convention**: Use clear, consistent naming
4. **Version Control**: Commit changes with meaningful messages

## Contributing

When adding new content:
1. Use descriptive file names
2. Include comments in DAX code
3. Document the purpose and context
4. Test queries before committing

## Notes

- PBIX files are excluded from version control (see .gitignore)
- Focus on code and documentation, not binary files
- Include sample data scenarios where helpful