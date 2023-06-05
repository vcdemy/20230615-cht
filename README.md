# 20230615

## 相關連結

* [Python基礎講義](https://docs.google.com/presentation/d/140dHWSexhiarrdZVQ1Rf466LgfAlBQz2CPRtrToCe2Q/edit?usp=sharing)
* [colab](https://colab.research.google.com/)
* [Pillow](https://pillow.readthedocs.io/en/stable/)
* [gradio](https://gradio.app/)
* [face recognition](https://github.com/ageitgey/face_recognition)
* [ChatGPT](https://chat.openai.com/)
* [DALL-E 2](https://openai.com/dall-e-2)
* [Midjourney](https://www.midjourney.com/)
* [Stable Diffusion Online](https://stablediffusionweb.com/)
* [D-ID](https://www.d-id.com/)

## 影像處理

* 開啟圖形檔
* 彩色轉單色
* 儲存圖形檔
* 繪製長方形

## gradio簡介

* gradio hello world
* 文字/圖片輸入/輸出

## 人臉偵測

```python
import face_recognition
image = face_recognition.load_image_file("your_file.jpg")
face_locations = face_recognition.face_locations(image)
```

## 人臉特徵偵測

```python
import face_recognition
image = face_recognition.load_image_file("your_file.jpg")
face_landmarks_list = face_recognition.face_landmarks(image)
```

## 人臉識別

```python
import face_recognition
known_image = face_recognition.load_image_file("biden.jpg")
unknown_image = face_recognition.load_image_file("unknown.jpg")

biden_encoding = face_recognition.face_encodings(known_image)[0]
unknown_encoding = face_recognition.face_encodings(unknown_image)[0]

results = face_recognition.compare_faces([biden_encoding], unknown_encoding)
```