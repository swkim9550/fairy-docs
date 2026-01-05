# Fairy 전시회 이미지 가이드

## 개요
marketing.html의 Gallery Section에 실제 Fairy 앱에서 생성된 전시회 이미지를 추가하기 위한 가이드입니다.

## 현재 상태
- **위치**: Gallery Section (line ~580-600)
- **현재 상태**: 이모지 플레이스홀더 사용 (🌅, 🏔️, 🌸, 🌊, 🌙)
- **필요한 작업**: 실제 전시회 이미지 5개로 교체

## 이미지 파일 구조

### 추가할 이미지 경로
```
images/
├── gallery/
│   ├── exhibition_01.jpg
│   ├── exhibition_02.jpg
│   ├── exhibition_03.jpg
│   ├── exhibition_04.jpg
│   └── exhibition_05.jpg
```

## HTML 수정 사항

### 현재 코드 (수정 전)
```html
<div class="gallery-preview">
    <div class="gallery-item">🌅</div>
    <div class="gallery-item">🏔️</div>
    <div class="gallery-item">🌸</div>
    <div class="gallery-item">🌊</div>
    <div class="gallery-item">🌙</div>
</div>
```

### 수정할 코드 (수정 후)
```html
<div class="gallery-preview">
    <div class="gallery-item">
        <img src="images/gallery/exhibition_01.jpg" alt="전시회 작품 1" style="width: 100%; height: 100%; object-fit: cover; border-radius: 16px;">
    </div>
    <div class="gallery-item">
        <img src="images/gallery/exhibition_02.jpg" alt="전시회 작품 2" style="width: 100%; height: 100%; object-fit: cover; border-radius: 16px;">
    </div>
    <div class="gallery-item">
        <img src="images/gallery/exhibition_03.jpg" alt="전시회 작품 3" style="width: 100%; height: 100%; object-fit: cover; border-radius: 16px;">
    </div>
    <div class="gallery-item">
        <img src="images/gallery/exhibition_04.jpg" alt="전시회 작품 4" style="width: 100%; height: 100%; object-fit: cover; border-radius: 16px;">
    </div>
    <div class="gallery-item">
        <img src="images/gallery/exhibition_05.jpg" alt="전시회 작품 5" style="width: 100%; height: 100%; object-fit: cover; border-radius: 16px;">
    </div>
</div>
```

## CSS 스타일 추가 권장사항

### 이미지 호버 효과 개선
```css
.gallery-item img {
    transition: all 0.3s ease;
    filter: brightness(0.9);
}

.gallery-item:hover img {
    filter: brightness(1.1);
    transform: scale(1.02);
}
```

## 작업 순서

1. **이미지 폴더 생성**
   - `images/gallery/` 폴더 생성

2. **이미지 파일 추가**
   - 5개의 전시회 이미지를 `images/gallery/` 폴더에 추가
   - 파일명: `exhibition_01.jpg` ~ `exhibition_05.jpg`

3. **HTML 수정**
   - marketing.html의 Gallery Section 수정
   - 이모지를 실제 이미지 태그로 교체

4. **테스트**
   - 브라우저에서 이미지 로딩 확인
   - 반응형 디자인 확인
   - 호버 효과 확인

## 이미지 요구사항

- **크기**: 최소 320x320px (정사각형 권장)
- **포맷**: JPG, PNG, WebP
- **용량**: 각 이미지 500KB 이하 권장
- **품질**: 웹 최적화된 고품질 이미지

## 다국어 지원

### alt 텍스트 다국어화 (선택사항)
```javascript
// translations 객체에 추가
galleryAlt1: '전시회 작품 1',
galleryAlt2: '전시회 작품 2',
// ... 등등
```

## 완료 후 확인사항

- [ ] 이미지가 올바르게 로드되는지 확인
- [ ] 모바일에서 레이아웃이 깨지지 않는지 확인
- [ ] 이미지 호버 효과가 작동하는지 확인
- [ ] 페이지 로딩 속도에 영향이 없는지 확인

---

**참고**: 이미지 파일을 추가한 후 이 가이드에 따라 HTML을 수정하면 Gallery Section에 실제 전시회 이미지가 표시됩니다.