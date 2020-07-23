---
title: "이미지 읽기"
date: 2020-07-23 11:00:00 -0400
categories: opencv
---

​```
import cv2

img_file = "./images/test_image.jpg"            # 이미지 파일의 경로
img = cv2.imread(img_file)                      # 이미지를 익어서 img 변수에 할당
                                                # imread 함수의 반환값은 Numpy 배열이다

if img is not None:
    cv2.imshow('IMG',img)                           # 'IMG'라는 창이름을 가진 사진을 화면에 표시
    cv2.waitKey(0)                                  # 키가 입력 될때까지 대기 n>0 인 n이 들어갈시 n(ms) 대기
    cv2.destroyAllWindows()                         # 창 모두 닫기
else:
    print("No Image file in directory" + img_file)


"""
img = cv2.imread(file_name [, mode_flag])

    -file_name : 이미지 경로, 문자열
    -mode_flag : cv2.IMREAD_COLOR 읽기 모드 지정
        -cv2.IMREAD_COLOR :컬러(BGR) 스케일로 읽기, 기본 값
        -cv2.IMREAD_UNCHANGED : 파일 그대로 읽기
        -cv2.IMREAD_GRAYSCALE : 그레이(흑백) 스케일로 읽기
    -img : 읽은 이미지, Numpy 배열

cv2.imshow(title, img) : 이미지를 화면에 표시
    -title : 창 제목, 문자열
    -img : 표시할 이미지, Numpy 배열

key = cv2.waitKey([delay])
    -delay : 키보드 입력을 대기할 시간(ms), 0 : 무한대(기본값)
    -key = 사용자가 입력한 키 값, 정수
    -대기시간 동안 키 입력 없을시 -1 반환

"""

​```
