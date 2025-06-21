# Git Setup Instructions for Power BI Project

## Initial Setup (One-time only)

### Prerequisites
- Git installed via Windows Terminal: `winget install --id Git.Git -e --source winget`
- GitHub account created
- Repository created on GitHub

### Git Configuration
```powershell
# Configure your identity
git config --global user.name "majorrabbid"
git config --global user.email "your.email@example.com"

# Verify configuration
git config --list --global
```

## Setting Up on New Computer

### Clone Repository
```powershell
# Navigate to desired location
cd C:\Users\[YourUsername]\Documents

# Clone the repository
git clone https://github.com/majorrabbid/pbi-AppMigrationDash.git

# Navigate into project
cd pbi-AppMigrationDash

# Verify everything is there
ls
```

## Daily Workflow

### Before Starting Work
```powershell
# Get latest changes from GitHub
git pull
```

### After Making Changes
```powershell
# Check what files have changed
git status

# Add all changes
git add .

# Commit with descriptive message
git commit -m "Added new DAX measures for migration tracking"

# Push to GitHub
git push
```

## Common Git Commands

### Check Status
```powershell
git status          # See what files are changed
git log --oneline   # See commit history
git remote -v       # See remote repository URLs
git branch -vv      # See branch tracking info
```

### Useful Commands
```powershell
# See what's different
git diff

# Add specific files only
git add filename.dax

# Commit with longer message
git commit -m "Title" -m "Detailed description of changes"

# See file contents
Get-Content filename.dax
```

## Project Structure

```
pbi-AppMigrationDash/
├── dax-queries/
│   ├── measures/              # Migration metrics and KPIs
│   ├── calculated-columns/    # App categorization and status
│   └── table-expressions/     # Migration analysis expressions
├── visuals-documentation/
│   ├── dashboards/            # Main dashboard screenshots
│   ├── reports/               # Migration report documentation
│   └── charts/                # Individual chart documentation
├── datasets/                  # Migration dataset schemas
├── reports/                   # Migration report metadata
├── templates/                 # Reusable dashboard patterns
├── README.md                  # Project overview
├── .gitignore                 # Files to ignore
└── SETUP-INSTRUCTIONS.md      # This file
```

## File Naming Conventions

### DAX Files
- Use descriptive names: `migration-progress-percentage.dax`
- Include comments in DAX code
- Organize by category (measures, calculated columns, etc.)

### Documentation Files
- Use markdown format (.md)
- Include screenshots with explanations
- Name files clearly: `dashboard-overview.md`

## Troubleshooting

### Common Issues

**"Failed to push" errors:**
```powershell
# Usually authentication issue, try:
git pull
git push
```

**"Not up to date" errors:**
```powershell
# Pull latest changes first
git pull
# Then push your changes
git push
```

**Forgot to pull before making changes:**
```powershell
# Stash your changes temporarily
git stash
# Pull latest changes
git pull
# Restore your changes
git stash pop
```

### Authentication Issues
- Make sure you're using correct GitHub username
- You may need to use personal access token instead of password
- Check repository permissions

## Best Practices

1. **Always pull before starting work**
2. **Commit frequently with meaningful messages**
3. **Don't commit .pbix files** (they're in .gitignore)
4. **Include comments in DAX code**
5. **Test DAX queries before committing**
6. **Keep documentation up to date**

## Repository URLs
- **GitHub Repository**: https://github.com/majorrabbid/pbi-AppMigrationDash
- **Clone URL**: https://github.com/majorrabbid/pbi-AppMigrationDash.git

## Contact
Created by: majorrabbid
Project: App Migration Dashboard
Platform: Power BI