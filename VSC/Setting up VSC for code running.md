For running the code :
- Go to command pallette and prompt Task : Configure Tasks and select modify tasks.json

For bulding C++ files paste this in the file :
```
	{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build cpp",
            "type": "shell",
            "command": "g++",  // Use g++
            "args": [
                "-g",  // Include debug information
                "${file}",  // The current file
                "-o",  // Output flag
                "${fileDirname}/${fileBasenameNoExtension}"  // Output executable name
            ],
            "group": {
                "kind": "build",
                "isDefault": true  // Set this as the default build task
            },
            "problemMatcher": ["$gcc"],  // Use the GCC problem matcher
            "detail": "Generated task for building C++ code."
        }
    ]
}
```

For building C pastes this in the file :
```
	{
    "label": "build c",
    "type": "shell",
    "command": "gcc",  // Use gcc
    "args": [
        "-g",  // Include debug information
        "${file}",  // The current file
        "-o",  // Output flag
        "${fileDirname}/${fileBasenameNoExtension}"  // Output executable name
    ],
    "group": {
        "kind": "build",
        "isDefault": true  // Set this as the default build task
    },
    "problemMatcher": ["$gcc"],  // Use the GCC problem matcher
    "detail": "Generated task for building C code."
}
```