리눅스에서 물리적 메모리(RAM)의 **용량이 가득 차게 됐을 때, 사용되는 여유 공간**을 의미합니다.
즉, 시스템이 처리하고 있는 **데이터가 있는데**, 이를 저장할 **RAM이 충분하지 않으면** **‘swap’ 공간에 이 데이터를 기록**하는 것입니다.

**스왑 공간**은 스왑 파티션에 사용되거나(권장 사항), 스왑 파일을 저장하는데 사용되며, 또는 스왑 파티션과스왑 파일이 함께 스왑 공간을 차지하는 것도 가능합니다.

스왑 공간의 최소 크기는 사용자의 컴퓨터 RAM 용량의 두 배나, 32 MB가 되어야 하며. 이중에 어느 용량이 크던지 간에 2048 MB (또는 2GB)를 넘어서는 안됩니다.

```js
// 사용자 컴퓨터 RAM의 2배 or 32MB = 스왑 공간의 최소 크기 < 2048MB
```
