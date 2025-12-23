# Sync Documentation - Core

This directory contains documentation about the core-updated repository.

## 📚 Repository Information

### Overview
- **Repository:** my-smart-homes/core (core-updated)
- **Upstream:** home-assistant/core
- **Status:** ✅ Previously synced
- **Purpose:** Home Assistant Core - main application logic

## 🔧 Key Components

The Core repository contains:
- **Home Assistant Core Logic**
  - All integrations and components
  - Device discovery and setup
  - Automation engine
  - State machine
  - Event system
  - Service registry

- **Integration Platform**
  - 2000+ integrations
  - Cloud services
  - Local devices
  - Smart home protocols
  - Media players
  - Sensors and switches

- **API Layer**
  - REST API
  - WebSocket API
  - Authentication system
  - Authorization framework

## 📊 Repository Status

- **Status:** ✅ Complete (previously synced)
- **Documentation:** Standard Home Assistant Core docs
- **Custom Changes:** None documented (standard fork)

## 🎯 Common Tasks

### Development
```bash
# Setup development environment
cd /home/fitl/git/me/outsource/mha/core-updated
python3 -m venv venv
source venv/bin/activate
pip3 install -e .

# Run tests
pytest tests/

# Run Home Assistant
hass --config config/
```

### Building Docker Image
```bash
# See build.yaml for build configuration
docker build -t my-smart-homes/core:latest .
```

## 📚 Documentation

### Official Docs
- **Developer Docs:** https://developers.home-assistant.io/
- **Component Development:** https://developers.home-assistant.io/docs/creating_component_index
- **Architecture:** https://developers.home-assistant.io/docs/architecture_index

### Important Files
- `homeassistant/` - Core application code
- `tests/` - Test suite
- `requirements.txt` - Python dependencies
- `build.yaml` - Build configuration
- `Dockerfile` - Container build
- `.devcontainer/` - Development container

## 🔗 Integration with Other Components

### Dependencies
- **Frontend** - UI served by Core
- **Supervisor** - Manages Core container
- **OS** - Provides runtime environment

### How It Fits
```
OS (Host System)
    ↓
Supervisor (Container Manager)
    ↓
Core (This Repository) ← Serves Frontend
    ↓
Integrations & Devices
```

## 🛠️ Custom Integration Development

### Adding Custom Integration
```bash
# Create custom integration
cd custom_components/
mkdir my_integration
cd my_integration

# Required files
touch __init__.py
touch manifest.json
touch config_flow.py
touch sensor.py  # or other platform
```

### Integration Structure
```
custom_components/my_integration/
├── __init__.py           # Integration entry point
├── manifest.json         # Integration metadata
├── config_flow.py        # Configuration flow
├── sensor.py            # Sensor platform
├── strings.json         # Translations
└── translations/        # Translations directory
    └── en.json
```

## 🔍 Finding Information

**For integration development:**
- Check `homeassistant/components/` for examples
- Read `CONTRIBUTING.md` for guidelines
- See developer docs for API reference

**For testing:**
- Review `tests/` directory
- Check `pytest` configuration
- See CI workflows in `.github/workflows/`

**For building:**
- Check `build.yaml` for build steps
- Review `Dockerfile` for container config
- See `requirements.txt` for dependencies

## 🔗 Related Documentation

- **Main report:** `../../COMPLETE_SYNC_REPORT.md`
- **Overview:** `../../SYNC_OVERVIEW.md`
- **Frontend docs:** `../../frontend-updated/sync-docs/`
- **OS docs:** `../../operating-system/sync-docs/`
- **Supervisor docs:** `../../supervisor/sync-docs/`

## 📝 Notes

This repository was previously synced with upstream. Since no custom sync documentation was created at that time, this README provides general information about the Core repository.

If a new sync is performed in the future, detailed sync documentation should be added to this directory similar to the OS and Supervisor repos:
- `SYNC_DOCUMENTATION.md` - Full sync details
- `CUSTOM_CHANGES.md` - Custom modifications
- `SYNC_QUICKREF.md` - Quick reference

## 🚀 Getting Started

### Quick Development Setup
```bash
cd /home/fitl/git/me/outsource/mha/core-updated

# Install dev dependencies
script/setup

# Run Home Assistant
script/develop

# Run specific tests
pytest tests/components/homeassistant/
```

### Common Commands
```bash
# Check code quality
pylint homeassistant/components/my_component/

# Format code
black homeassistant/

# Type checking
mypy homeassistant/

# Run linting
pre-commit run --all-files
```

---

**Last Updated:** December 23, 2025  
**Repository:** core-updated (previously synced)
