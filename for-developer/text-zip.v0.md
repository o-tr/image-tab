# TextZip v0
## 定義
```typescript
type Rect = {
  width: number;
  height: number;
}

type ManifestItem = {
  path: string;
  rect: Rect
}

type Manifest = ManifestItem[];
```
## サンプルデータ
```
[
  {
    "path": "0.rawimage",
    "rect": {
      "width": 612,
      "height": 792
    }
  },
  {
    "path": "1.rawimage",
    "rect": {
      "width": 612,
      "height": 792
    }
  }
]
```
