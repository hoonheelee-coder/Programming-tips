# Programming-tips

## Visual Studio Code
### GCC compiler
Error: "The preLaunchTask 'C/C++: g++.exe build active file' terminated with exit code 1"

이러한 에러 메세지가 나타날 경우 아래의 절차를 따라서 해 보세요.   
방법 1. 실행하는 c 파일을 포함하는 폴더 안에 .vscode 가 있으면 삭제하고 재실행을 해 보세요.   
   
방법 2. 컴파일러를 제대로 연결하였는지 확인 해 보세요.   
<pre>
    <code>
</pre>
{
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: gcc.exe build active file",
            "command": "C:\\msys64\\ucrt64\\bin\\gcc.exe",
            "args": [
                "-fdiagnostics-color=always",
                "-g",
                "${file}",
                "-o",
                "${fileDirname}\\${fileBasenameNoExtension}.exe"
            ],
            "options": {
                "cwd": "C:\\msys64\\ucrt64\\bin"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "Task generated by Debugger."
        }
    ],
    "version": "2.0.0"
}
</code>
</code>
