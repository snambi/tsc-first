# Typescript Project

The goal of this project is to explore typescript and tools necessary to develop and manage typescript SDLC.

## Basic VSCode Setup

Followed this tutorial for basic setup: https://www.youtube.com/watch?v=4zdBk6wisxc 

But the it is not sufficient.

### Additional Setup

1. Add additional launch configuration. add the following into `launch.json`

```json

    {
            "type": "node",
            "runtimeVersion": "20.5.1",
            "request": "launch",
            "name": "Debug TS",
            "skipFiles": [
                "<node_internals>/**"
            ],
            "program": "${workspaceFolder}/src/index.ts",
            "preLaunchTask": "tsc: build - tsconfig.json",
            "sourceMaps": true,
            "smartStep": true,
            "internalConsoleOptions": "openOnSessionStart",
            "runtimeExecutable": "node",
            "outFiles": [
                "${workspaceFolder}/dist/**/*.js"
            ]
        }
```

2. Install `nvm` 
3. Make sure `nvm` installation has the node runtime mentioned the `launch.json`
   
```bash
nvm ls-remote
nvm install v20.5.1
nvm ls
nvm use v20.5.1
```

After all of the above, visual debugging for `typescript` works in `vscode`.

# For debugging nestJS

Follow this https://dev.to/gentax/nestjs-right-settings-for-debugging-kl0#:~:text=open%20to%20VSCode%20settings%2C%20then,select%20Always%20from%20the%20dropdown.&text=It%20enables%20debug%20and%20console. 
