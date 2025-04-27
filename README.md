# 42 Header Generator

A live template for CLion that generates the standard 42 School header for C/C++ files using Velocity templates.

---

### Description

This repository provides a Velocity template that automatically creates 42 School’s distinctive file headers, complete with dynamic spacing to maintain perfect visual alignment, no matter the filename or username length.

---

## Table of Contents

- [Description](#description)
- [Features](#features)
- [How to implemente](#how-to-implemente)
- [Usage](#usage)
- [Example Output](#example-output)
- [License](#license)

---

### Features

- Automatic padding to maintain perfect visual alignment.
- Fully customizable with your username and school location.
- Compatible with any IDE supporting Velocity templates (e.g., CLion, VSCode, Vim).

---

## How to implemente 

**1. Add the Template to CLion:**

- Go to `settings`>`Editor`>`Code Style`>`File and Code Templates`.
- Open the `Includes` tab.
- Click `+` or `add` to add a new template.
- Paste the provided code.
- Name it (e.g, `42Header`) and click `Apply`.

**2. Integrate into Your File Templates:**
- Still in `File and Code Templates`, go to the `Files` tab.
- Select templates such as `C++ Class`, `C++ Class Header`, and `C++ Module File`.
- At the top of each template, add:
    ```cpp
  #parse("Name of your template")`
- Replace `"Name of your template"` with the same name you chose (e.g., 42Header).
- Click `Apply`.

Repeat for any file types you want (e.g., .c files if needed).

Note: If you use the 42Header plugin for CLion, it may already manage .c files.


## Usage

Before using the template, set your personnal information:

```
#set($USER = "yourusername")    - e.g. "maximart"
#set($CITY = "yourcity")        - e.g. "lyon"
#set($EXT = "extension")        - e.g. ".fr"
```

The template expects these IDE-provided variables:
```
$FILE_NAME                      - Name of the current file
$YEAR, $MONTH, $DAY             - Current date
$HOUR, $MINUTE, $SECOND         - Current time
```
---

### Example Output

```cpp
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   example.cpp                                        :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: maximart <maximart@student.42lyon.fr>      +#+  +:+       +#+        */
/*                                                +#+#+#+#+#+   +#+           */
/*   Created: 2025/04/27 12:00:00 by maximart          #+#    #+#             */
/*   Updated: 2025/04/27 12:00:00 by maximart         ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */
```

---

### License

This project is released under the MIT License. See the LICENSE file for details.











