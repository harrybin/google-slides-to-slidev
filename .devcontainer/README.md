# Dev Container Configuration

This directory contains the development container configuration for GitHub Codespaces and VS Code Dev Containers.

## What's Included

- **Python 3.11**: Base development environment
- **Node.js LTS**: Required for Slidev
- **Git**: Version control support
- **Python packages**: Automatically installed from `requirements.txt`
- **Slidev**: CLI and Seriph theme pre-installed globally
- **VS Code Extensions**:
  - Python language support
  - Pylance for enhanced Python features
  - Markdown editing and linting

## Usage

### GitHub Codespaces

1. Click the "Code" button on the repository
2. Select "Codespaces" tab
3. Click "Create codespace on main"
4. Wait for the container to build and start
5. All dependencies will be automatically installed

### VS Code Dev Containers

1. Install the "Dev Containers" extension in VS Code
2. Open the repository in VS Code
3. Press `F1` and select "Dev Containers: Reopen in Container"
4. Wait for the container to build and start

## Features

- **Port Forwarding**: Port 3030 is automatically forwarded for Slidev preview
- **Auto-install**: Python and Node.js dependencies are installed automatically
- **Pre-configured**: VS Code settings optimized for Python and Markdown development

## Testing the Setup

After the container starts, you can test the environment:

```bash
# Check Python installation
python --version

# Check pip packages
pip list

# Check Node.js installation
node --version

# Check Slidev installation
slidev --version

# Run the converter (with a .pptx file)
python slidev_converter.py --pptx "your-file.pptx" --output ./output
```

## Customization

Edit `devcontainer.json` to:
- Change Python version (modify the `image` field)
- Add more VS Code extensions
- Install additional tools
- Modify post-creation commands
