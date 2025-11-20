# Sloves Starter 🚀

**Python Simple Launcher For Virtual Environment Scripts**

---

## What's This?

Sloves Starter is a single-file Python script launcher that handles virtual environments and dependencies automatically.
The goal is to not take up space in the project and to ensure that all Python packages are for the main project.

```bash
python Sloves_Starter.py
```

## Features

- ✅ **Auto Virtual Environment** - Creates/activates venv automatically
- ✅ **Smart Dependency Management** - Installs requirements.txt or config-based packages
- ✅ **Interactive Script Selection** - Choose scripts from your project
- ✅ **Cross-Platform** - Windows, Linux, macOS ready
- ✅ **Configuration Driven** - JSON config for all settings
- ✅ **Performance Monitoring** - Nanosecond-level runtime tracking

## Quick Start

1. Drop `Sloves_Starter.py` in your project
2. (Optional) Create `config.json` for customization
3. Run: `python Sloves_Starter.py`

## Example Config

```json
{
    "title": "Sloves Python Script Starter",
    "console_title": "Sloves Python Script Starter",
    "process_title": "Python Script",
    "process_exit_title": "Sloves Python Script Starter",
    "exit_title": "Sloves Python Script Starter",
    "python_name": {
        "windows": "python",
        "linux": "python3",
        "macos": "python3",
        "jvm": "python3",
        "default": "python3"
    },
    "pip_name": {
        "windows": "pip",
        "linux": "pip3",
        "macos": "pip3",
        "jvm": "pip3",
        "default": "pip3"
    },
    "requirements": [
        {
            "name": "requests"
        },
        {
            "name": "numpy",
            "version": "1.19.5"
        }
    ],
    "requirements_file": "requirements.txt",
    "cwd": "D:\\Projects\\Python\\Sloves_Starter",
    "work_directory": "D:\\Projects\\Python\\Sloves_Starter",
    "use_venv": true,
    "venv_prompt": "venv",
    "script_name": null,
    "argument": null,
    "restart": false,
    "reselect": false,
    "run_cmd_need_to_ask": true,
    "run_cmd_ask_default_values": {},
    "divider_line_char": "=",
    "inject_environment_variables": {},
    "text_encoding": "utf-8",
    "print_return_code": true,
    "print_runtime": true,
    "automatic_exit": false,
    "allow_print": true
}
```
When it can't find one, it tries to create one.

## Exit Codes

| Code | Description |
| --- | --- |
| 0 | SUCCESS |
| 1 | CONFIG_NOT_FOUND |
| 2 | CONFIG_DECODE_ERROR |
| 3 | CONFIG_ENCODE_ERROR |
| 4 | CONFIG_WRITE_ERROR |
| 5 | CONFIG_READ_ERROR |
| 6 | CONFIG_PERMISSION_ERROR |
| 7 | SCRIPT_NOT_FOUND |
| 8 | SCRIPT_NAME_TYPE_ERROR |
| 9 | SCRIPT_NAME_IS_EMPTY |
| 10 | SCRIPT_NAME_NOT_PROVIDED |
| 11 | USER_TERMINATED |
| 255 | UNKNOWN_ERROR |

When the child process runs, the return value of the child process is returned.
When the program returns an `UNKNOWN_ERROR`, it writes the traceback to the `Traceback.txt` file

## Why 48KB?

Because it includes:
- Virtual environment manager
- Interactive CLI interface  
- Package dependency resolver
- Cross-platform compatibility layer
- Configuration system
- Performance metrics
- Error handling framework

---

## License

[MIT License](LICENSE)