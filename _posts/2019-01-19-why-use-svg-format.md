---
title: "[HTML] 로고나 아이콘에 SVG를 사용해야하는 이유"
date: 2019-01-19 14:30:00 -0400
categories: HTML SVG 
tags: SVG
---

로고나 아이콘에 왜 SVG를 사용해야할까?
=======

많은 분들께서 홈페이지에 이미지를 올릴 경우에 png, gif, jpg 형식을 주로 사용하시는 걸로 압니다.
아시겠지만 위와 같은 확장자는 픽셀을 기반으로 하고 있기때문에 이미지가 클수록, 스케일이 클수록 그 용량이 커집니다.

하지만, SVG의 경우에는 벡터를 기반으로 하고 있기때문에 이미지에 대한 정보를 좌표로 저장하고 있습니다.
따라서, 크기가 엄청나게 커지더라도, 좌표로만 인지해서 그 안에 색을 채우기 때문에 용량의 제한은 물론, 크기의 제한도 없습니다.
사실 SVG 그래픽안에 이미지에 대한 모든 정보를 가지고 있고, 수정도 가능하기때문에 거의 원본이라고 생각하시면 됩니다.

(좀 복잡한 형태의 로고들은, IE11에서도 가장자리가 깨져보이는 형태를 많이 보았습니다. 
그래서 그떄 SVG의 필요성을 절실히 깨달은거죠.)

하지만 SVG에 대해 낯설게 느끼실 분들이 많이 계실겁니다. 갑자기 나온 새로운 형식아니냐고 생각하실 수 도 있지만,
사실 SVG는 근 10년전부터 w3c 에서 표준으로 지정된 방식입니다.
그런데 왜 낯서냐구요? 우리에게 친숙했던 IE에서 8버전 이하로는 지원을 하지 않았기 때문입니다.
그러면 지금도 IE8 이하로는 지원이 안되는거 아니냐? 그런데 왜 SVG를 써야하냐고 물으실 수 있습니다.

기술은 발전하고 있고 더 깔끔하고 가벼운 홈페이지를 위해 SVG를 사용해야하기 때문입니다. 
그리고 IE8 이하는 javascript 나 css로 png,jpg 등의 기존에 사용하시던 이미지의 포맷을 사용하시면 됩니다.

물론! 그렇다고해서 모두 SVG를 사용해야한다는 것은 아닙니다. 사진이라던지 다양한 그래픽을 사용하는 곳에는
png, jpg 등의 확장자가 좋습니다. SVG로 하나하나 다 사진에 있는 그 컬러들을 좌표로 잡게 되면 그 구성이 복잡해서 SVG용량또한 커질 테니까요.

