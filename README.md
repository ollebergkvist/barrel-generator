# Barrel Generator Script

This repository contains a script for generating barrel files in a directory structure. The script recursively generates `index.ts` files, also known as barrel files, in each subdirectory, including the root directory, if applicable. Barrel files help organize and streamline module imports in large codebases.

## Usage

To use the script, follow the instructions below:

1. Clone the repository:

   ```shell
   git clone https://github.com/olle-bergkvist/barrel-generator-script.git
   ```

2. Run the script:

   ```
   ./generate_barrel.sh <folder>
   Replace <folder> with the path to the root folder where you want to generate the barrel files.
   ```

The script will generate index.ts files in each subdirectory, including the root folder if it contains subdirectories.

For example, suppose you have the following directory structure:

```
components/
└─ atoms/
   ├─ Button/
   │  └─ Button.ts
   └─ Input/
      └─ Input.ts
```

Running the script with ./generate_barrel.sh components will generate the following barrel files:

```
components/
├─ atoms/
│  ├─ Button/
│  │  ├─ Button.ts
│  │  └─ index.ts
│  ├─ Input/
│  │  ├─ Input.ts
│  │  └─ index.ts
│  └─ index.ts
└─ index.ts
```

The generated index.ts files act as barrel files and export all the modules in each respective directory, allowing for cleaner and more efficient imports.

Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.
