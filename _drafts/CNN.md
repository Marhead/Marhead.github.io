# CNN

## Convoltuion

이미지위에서 stride 값 만큼 filter(kernel)을 이동시키면서 겹쳐지는 부분의 각 원소의 값을 곱해서 모두 더한 값을 출력으로 하는 연산 

- stride : filter를 한번에 얼마나 이동 할 것 인가.
- padding : zero-padding, 일종의 패드를 씌운다. 이미지 상하 좌우에 0으로된 값들이 주변을 둘러 쌈 

*Convolution의 output 크기 계산*

$$ Output size = {input size - filtersize +(2 * padding) \over stride} + 1 $$

## Neuron과 Convolution

filter = perceptron의 input의 weight값으로 연산하여 perceptron의 input으로 작용



## Pooling

Image size를 줄이기 위해 사용, 혹은 fully-connect연산을 줄이기 위해서도 사용

- Max Pooling : 지정된 영역의 가장 큰 값을 리턴
- Average Pooling : 지정된 영역의 평균값을 리턴

cross-correlation <-> autocorrelation

뒤집고 계산하면 => convolution

안뒤집고 계산하면 => cross-correlation

안뒤집고 계산해서 ==>> cross-correlation

## MNIST에 CNN 적용

### 학습 단계

---

1. 라이브러리 가져오기
2. GPU사용 설정
3. 학습에 사용되는 parameter 설정
4. 데이터셋을 가져오고 loader만들기
5. 학습 모델 만들기(class CNN(torch.nn.Module))
6. Loss function (Criterion)을 선택하고 최적화 도구 선택(optimizer)
7. 모델 학습 및 loss check(Criterion의 output)
8. 학습된 모델의 성능을 확인

결과, 정확도 98.5%

더 깊게 레이어를 쌓는다면?

layer 4, 5단계를 더 쌓았더니 정확도가 떨어짐. == 효율적으로 쌓는게 중요하다는 증거

## Visdom 사용 방법

~.~.~

## Imagefolder

1. 나만의 데이터 셋 준비하기
2. torchvision.datasets.ImageFolder 으로 불러오기
3. transforms적용하여 저장하기 origin_data -> train_data



# Advanced CNN

going deeper with convolutions

CNN의 네트워크가 깊어지면 깊어질수록, 더 많은 레이어를 가질 수록 성능이 좋아지는 것은 분명하다. 그러나, 네트워크가 깊어질 수록 학습해야하는 파라미터의 수가 늘어난다는 문제점이 있다. 깊은 곳에 위치한 convolution 연산에서 이러한 특징이 두드러진다.

대부분의 cnn에서 이미지가 합성연산을 거치게되면 될수록, channel은 커지고, height와 width는 줄어든다.

**Network in Network**

일반적인 convolution layer는 필터가 움직이면서 연산 수행 -> 활성화 함수 -> 결과

그러나, 만약 데이터 분포가 비선형적이라면?

문제를 해결하기 위해 중간에 곱, 합연산을 바로 하는것이 아니라, 중간에 MLP를 대입.

==>> Network in Network(NIN)

MLP들 또한 convolution의 필터들과 같이 역전파를 통해 학습, 그자체가 깊은 구조를 가질 수 있음.

마지막에는 Fully-Connected Layer가 아니라, Global Average Pooling을 넣음. -> 오버피팅 방지 

VGG Network 직접 만들기

