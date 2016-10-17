# Eland Plugin - Printer
Printer 플러그인은 Cordova Plugin으로 iOS와 Android를 지원하고 있다.
Eland Printer는 cordova-plugin-printer(https://github.com/katzer/cordova-plugin-printer)를 기반으로하고 있다.
기존 플러그인에 PDF 파일을 인쇄할 수 있도록 추가 수정한 플러그인이다.

## 설치 방법
```
cordova plugin add https://github.com/june1249/eland-plugins-printer.git
```

## 사용방법
* Web
```
controllerModule.controller('MyCtrl', function($scope, $cordovaPrinter) {
	// HTML소스
    var doc = "<html> ... </html>";
    $cordovaPrinter.print(doc);
    
    // URL Web Page
    $cordovaPrinter.print("https://google.com");
    
    // PDF File
    var file = cordova.file.externalApplicationStorageDirectory + "1234.pdf";
    $cordovaPrinter.print(file);
});
```
