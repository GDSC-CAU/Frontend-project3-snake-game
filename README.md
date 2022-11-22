# 1. 구현사항

-   `canvas` api를 활용하여 그래픽을 표현해봅시다.
-   정사각형 보드판(ex: `50` X `50`) 규격으로 제작합니다.
-   플레이 / 일시정지 / 다시시작 / 스코어보드 표시 UI가 존재해야합니다!

-   스네이크의 **성장과정은** 다음과 같습니다.

    1. 처음 스네이크의 길이는 `N`(`2 <= N <= 5`)입니다.
    2. 일정 시간 간격(`t`)마다 스네이크는 현재 키보드 방향으로 이동합니다.
    3. 정사각형 보드판에서 랜덤으로 먹이가 생성됩니다.
    4. 먹이를 먹는 순간 스네이크의 길이는 1 추가 되며, 새로운 먹이가 다시 생성됩니다.

-   스네이크의 **움직임은** 다음과 같습니다.

    1. 키보드의 방향(상/하/좌/우)에 맞추어 움직입니다.
    2. 현재 방향의 반대 방향으로는 움직일 수 없습니다.
    3. 벽에 닿으면 죽습니다.
    4. 머리가 몸에 부딪히면 죽습니다.

-   **점수계산은** 다음과 같습니다.(점수 획득량, `ß1` `ß2`는 임의로 설정)
    -   스네이크 먹이를 먹은 수 `+ ß1`
    -   스네이크 생존시간 초당 `+ ß1`

**play demo버전**을 확인해보세요! (플레이 방식을 확인해보세요!)

[google snake game](https://www.google.com/search?q=snake+game&sxsrf=ALiCzsZe95SS4YtnXhr74MqsZI8q34Qgjw%3A1668488553361&ei=aR1zY5DQFZOm1e8P5oK2iAs&ved=0ahUKEwjQqKOctK_7AhUTU_UHHWaBDbEQ4dUDCA8&uact=5&oq=snake+game&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIFCC4QgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQ6CggAEEcQ1gQQsAM6BAguEEM6CwgAEIAEELEDEIMBOggILhCABBDUAkoECE0YAUoECEEYAEoECEYYAFCmAljyB2DyCWgBcAF4AIABdogBsgSSAQMwLjWYAQCgAQHIAQrAAQE&sclient=gws-wiz-serp)

# 2. 생각해보기

-   구글링 보다는 막히는 부분을 함께 생각해서 해결해봅시다🙂!
-   `requestAnimeframe` 혹은 `setInterval` api를 사용하면서, 두 api의 차이점을 이해하고 적용해봅시다.
-   `fucntion` 혹은 `class`를 한가지 기능만을 하도록 최소 단위로 쪼개봅시다!
