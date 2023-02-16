---
title:  "[VSCODE] VSCODE에서 Spring Boot Profile 사용"

categories:
  - ide
tags:
  - [ide, vscode]

toc: true
toc_sticky: true
 
date: 2023-02-15
last_modified_at: 2023-02-15
---
# 1. 실행 및 디버그 탭 수정
```json
#launch.json
{
    // IntelliSense를 사용하여 가능한 특성에 대해 알아보세요.
    // 기존 특성에 대한 설명을 보려면 가리킵니다.
    // 자세한 내용을 보려면 https://go.microsoft.com/fwlink/?linkid=830387을(를) 방문하세요.
    "version": "0.2.0",
    "configurations": [
        {
            "type": "java",
            "name": "Launch Current File",
            "request": "launch",
            "mainClass": "${file}"
        },
        {
            "type": "java",
            "name": "Launch Application[local]",
            "request": "launch",
            "mainClass": "mb.fw.atb.AtbApplication",
                    ...
            "args": "--spring.profiles.active=local" // 해당 args 에 사용할 profile 지정
        },
        {
            "type": "java",
            "name": "Launch Application[INFO]",
            "request": "launch",
                    ...
            "args": "--spring.profiles.active=info" // 해당 args 에 사용할 profile 지정
        }
    ]
}
```
