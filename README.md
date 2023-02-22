# find_similar_path

A bash script to filter paths based on the similarity of their subdirectory and file name components using Jaccard similarity.

## Usage

```
Usage: find_similar_path [-h|--help] <base_dir> [threshold] [format_string]
Filter paths based on the similarity of their subdirectory and file name components using Jaccard similarity.

<base_dir>      The base directory to search for paths
[threshold]     The Jaccard similarity threshold (default: 0.7)
[format_string] The format string for the output (default: '{path}')
-h, --help      Show this help message and exit
```

## Examples

To filter paths in the current directory with a Jaccard similarity threshold of 0.8 and output the full path:

```
find_similar_path . 0.8
```

To filter paths in the directory `/path/to/base_dir` with a Jaccard similarity threshold of 0.5 and output the first subdirectory and file name without the '.md' extension:

```bash
find_similar_path /path/to/base_dir 0.5 '{dir}\t{basename}'
```

## Requirements

- bash
- find
- Python3

## Installation

You can download the script and make it executable:

```sh
curl -O https://raw.githubusercontent.com/Mako-da/find_similar_path/main/find_similar_path
chmod +x find_similar_path
```

Or, you can clone the repository and add it to your `PATH`:

```sh
git clone https://github.com/Mako-da/find_similar_path.git
export PATH=$PATH:/path/to/find_similar_path
```

## Contributing

If you find a bug or have a feature request, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT](LICENSE) license.