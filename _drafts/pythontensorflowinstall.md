## 가상 환경 만들기(권장사항)
저장할 .\venv 디렉터리를 만들어 새로운 가상 환경 구축
```shell
python -m venv --system-site-packages .\venv
```
가상환경 활성화
```shell
.\venv\Scripts\activate
```

```shell
pip install --upgrade pip

pip list  # show packages installed within the virtual environment
```
가상환경 종료
```shell
deactivate  # don't exit until you're done using TensorFlow
```



https://kangbk0120.github.io/articles/2018-01/inception-googlenet-review

https://blueskyvision.tistory.com/504

https://m.blog.naver.com/laonple/221229726012

https://blueskyvision.tistory.com/644

https://ganghee-lee.tistory.com/41

https://medium.com/@msmapark2/vgg16-%EB%85%BC%EB%AC%B8-%EB%A6%AC%EB%B7%B0-very-deep-convolutional-networks-for-large-scale-image-recognition-6f748235242a