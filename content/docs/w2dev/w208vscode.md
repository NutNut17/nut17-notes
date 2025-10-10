---
title: "VS Code"
description: ""
summary: ""
date: 2025-07-09T23:44:01+08:00
lastmod: 2025-07-09T23:44:01+08:00
weight: 208
draft: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### VS Code

#### Shortcuts

| Description | Shortcut |
| - | - |
| Next cursor on same highlighted word | Ctrl + D |
| Move line up | Alt + Up |
| Copy line up | Shift + Alt + Up |
| Formating | Shift + Alt + F |
| Setting | Ctrl + , |
| Close folder | Ctrl + K, F |
| Command Palette | Ctrl + Shift + P |
| Expand Current Block | Ctrl + Shift + \] |
| Fold Recursively | Ctrl + K, Ctrl + \[ |
| Copy Path | Shift + Alt + C |
| Copy Relative Path | Ctrl + K, Ctrl + Shift + C |

### Debug

Inspect `variables` and custom `watch` for deeper debug analysis.

| Icon | Action                      | What It Does                                     |
| ---- | --------------------------- | ------------------------------------------------ |
| ▶️   | **Continue / Resume (F5)**  | Runs until next breakpoint or program end        |
| ⏭️   | **Step Over (F10)**         | Execute next line **without entering** functions |
| ⤵️   | **Step Into (F11)**         | **Enter** called function to debug inside it     |
| ⤴️   | **Step Out (Shift+F11)**    | Finish current function and go back up one level |
| 🔁   | **Restart (Ctrl+Shift+F5)** | Restarts the debugging session                   |
| ⏹️   | **Stop (Shift+F5)**         | Ends debugging                                   |

Debug Configuration allows different types of debug methods.

```json {title=".vscode/launch.json"}
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python Debugger: Stop on Entry",
      "type": "debugpy",
      "request": "launch",
      "program": "${file}",
      "console": "integratedTerminal",
      "args": "${command:pickArgs}",
      "stopOnEntry": true,
      "cwd": "${workspaceFolder}"
    }, 
    {
      "name": "Python Debugger: Another config",
      "type": "debugpy",
      "request": "launch",
      "program": "tools/train.py",
      "console": "integratedTerminal",
      "args": [
        "configs/faster_rcnn/faster-rcnn_r50_fpn_1x_coco.py",
        "--work-dir",
        "./work_dirs/my_exp1",
      ]
    }
  ]
}
```
