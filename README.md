# GitHub Project Manager

A simple web tool to import tasks from CSV files into GitHub Projects V2 and manage existing project tasks.

## 🚀 Features

- **📤 CSV Import**: Bulk import issues from CSV files directly into GitHub Projects V2
- **📋 Task Management**: View, select, and delete existing project tasks
- **🔍 Smart Repository Detection**: Automatically load your repositories with descriptions
- **💡 User-Friendly Interface**: Clean, intuitive design with helpful tooltips
- **🌐 Client-Side Only**: No server required - runs entirely in your browser

## 📋 Quick Start

1. **Download** or clone this repository
2. **Open** `uploader.html` in your web browser
3. **Create** a GitHub Personal Access Token (see permissions below)
4. **Enter** your token and start importing/managing tasks!

## 🔑 GitHub Token Setup

You'll need a **Personal Access Token (Classic)** with these permissions:

| Scope | Purpose |
|-------|---------|
| `repo` | Create issues in repositories |
| `project` | Read and write Projects V2 |

**How to create:**

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token"
3. Select the `repo` and `project` scopes
4. Copy the token and paste it in the tool

> **Note**: For public repositories only, you can use `public_repo` instead of `repo`

## 📊 CSV Format

Your CSV file should follow this simple structure:

```csv
title,body
Setup project,Basic project configuration and structure
Add authentication,Create login and register screens with validation
Database design,"Create users, groups, and questions collections"
Push notifications,Configure FCM and handle permissions
```

### Rules

- ✅ **First row**: Header (will be ignored)
- ✅ **First column**: Issue title (required)
- ✅ **Second column**: Issue description (optional)
- ✅ **Quotes**: Use quotes around descriptions that contain commas

## 🎯 How to Use

### Import CSV Tasks

1. Enter your GitHub Personal Access Token
2. Load your projects and select the target project
3. Load your repositories and select where to create issues
4. Upload your CSV file
5. Click "Import" and watch the magic happen!

### Manage Existing Tasks

1. Switch to the "Manage Tasks" tab
2. Load your projects and select one
3. Click "Load tasks" to see all project items
4. Select tasks you want to remove and click "Delete selected"

## 💡 Use Cases

- **Project Planning**: Import your project roadmap from spreadsheets
- **Issue Migration**: Move tasks between different project management tools
- **Bulk Operations**: Create multiple related issues quickly
- **Project Cleanup**: Remove completed or obsolete tasks in bulk
- **Team Collaboration**: Import tasks created by team members in CSV format

## 🛠️ Technical Details

- **Client-side only**: No data leaves your browser
- **GitHub API**: Uses official GitHub REST and GraphQL APIs
- **No installation**: Just open the HTML file
- **Modern browsers**: Works with Chrome, Firefox, Safari, Edge

## 📝 Examples

### Basic CSV Example

```csv
title,body
Setup development environment,Install Node.js and required dependencies
Create project structure,Set up folders and basic configuration
Implement authentication,Add user login and registration functionality
```

### Advanced CSV Example

```csv
title,body
"Setup Expo React Native project","- Install Expo CLI
- Initialize project with TypeScript
- Configure navigation and state management"
"Database schema design","Create Firestore collections:
- Users (auth, profile)
- Projects (metadata, settings)
- Tasks (title, status, assignee)"
```

## 🤝 Contributing

Contributions are welcome! This is a simple, single-file tool that's easy to understand and modify.

1. Fork the repository
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📄 License

MIT License - feel free to use this tool for personal or commercial projects.

## ⚠️ Important Notes

- **Token Security**: Your token is only used in your browser and never stored or transmitted anywhere else
- **Rate Limits**: GitHub API has rate limits - for large imports, the tool will respect these limits
- **Project V2 Only**: This tool works with GitHub's newer Projects V2, not the classic Projects
- **Issue Creation**: Issues are created in the repository you specify, then added to the project

## 🆘 Troubleshooting

**"No accessible projects found"**

- Make sure your token has the `project` scope
- Verify you have access to Projects V2 (not classic projects)

**"Repository not found"**

- Check that your token has `repo` or `public_repo` scope
- Ensure the repository name is correct

**"CSV parsing errors"**

- Make sure your CSV follows the format guidelines
- Use quotes around descriptions containing commas
- Check for proper line endings

---

**Made with ❤️ for the GitHub community**
