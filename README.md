# Youtube sample website (version 1)
1. Website's address: https://yoons4.github.io/youtube-website-version-1/
2. 컴퓨터 언어: React.
3. 설명: 보통 YouTube Website처럼 모양이 비슷하지만 보통 엡사이트가 가져야 할 기능들을 충분히 가지고 있다.

***

## 유투브 해더

--첫번째는 유투브 해더가 있었다. 기능이 없기는 하나 모든 유투브 엡사이트의 CSS Style의 기본 하나다. 쉽게 말하자면 자신에 대한 표현이다.
<img width="1439" alt="Screenshot 2023-02-22 at 3 11 50 PM" src="https://user-images.githubusercontent.com/44684815/220537846-1dfdc82b-f920-4118-98b8-7451790e26b8.png">

***

## 유투브 비디오

--비디오 이름은 "VID-20220119-WA0027 (1).mp4". 이 페이지를 열자

    <section className = "player">
        <video src = {videoSangha} controls autoPlay muted></video>
    </section>

--내가 왜 "controls autoPlay muted"를 더했나면 엡사이트를 열자마자 비디오가 직접 시작해야 하니까.

***

## 페이지 크기

--그리고 Responsive Web Design에 대한 Youtube sample website의 페이지 크기 규칙이 있다.

    @media only screen and (min-width: 768px){
        .infoAndUpNext{
            flex-direction: row;
            margin: 12px 0;
        }
    }
    
--만약 내가 그 엡사이트 페이지 넓이 (min-width)를 768px보다 더 줄인다면 비디오 아래에 있는 코드 section들의 위치 순서가 세로로 줄 쓰게된다.

<img width="751" alt="Screenshot 2023-02-22 at 3 40 16 PM" src="https://user-images.githubusercontent.com/44684815/220542761-9ae69735-ccd9-4387-8494-ee62cfe81b09.png">
 



--그 반대로 앱사이트의 넒이가 768px이거나 보다 더 큰다면 비디오 아래에 있는 section들의 위치 순서가 가로로 정리 되어진다.

<img width="1440" alt="Screenshot 2023-02-22 at 3 39 41 PM" src="https://user-images.githubusercontent.com/44684815/220542653-6542cf44-b989-43a9-b49f-0b3289a2f976.png">

***

## I like this / I dislike this.

--나는 이 진짜 버튼처럼 생긴 버튼을 만들었어요.
<img width="173" alt="Screenshot 2023-02-22 at 4 38 29 PM" src="https://user-images.githubusercontent.com/44684815/220553957-acb738db-e2c4-4c11-a4fc-8c66b21edcd0.png">

--파란색 버튼은 "I like this" button. 

--빨간색 버튼은 "I displike this" button.

--버튼들 사이에는 숫자가 있는데 이 비디오에 찬성하는 사람들의 수를 나타냄.

***

## Subscribe button 역할

--나는 이제 "Subscribe" 버튼을 만들었는데 .....<img width="462" alt="Screenshot 2023-02-22 at 4 50 17 PM" src="https://user-images.githubusercontent.com/44684815/220556336-e52f86e2-1981-4ce8-bc97-88d39f2a6905.png">

--이 빨간 글짜를 누르면 contextmenu가 나온다. 이 메뉴에 "Subscribe", "Unsubscribe" 버튼들이 나온다. "Subscribe"를 누르면 나에 대한 subscriber 수가 증가하고 반대로 "Unsubscribe"를 누르면 subscribe 수가 줄어든다.

--상황에 따라 빨간 글짜가 바뀜.

***

## Share, Save, Report 버튼들

--내꺼와 진짜 유투브 엡사이트의 사이에서 이 기능들의 특징은 거이 차이가 없다. 왜냐하면 그것들을 누를 때마다 Modal Menu가 나오기 때문이다. 

1. Share: <img width="1440" alt="Screenshot 2023-02-22 at 5 04 13 PM" src="https://user-images.githubusercontent.com/44684815/220559287-8d39e0a6-92e5-47f9-9375-6cc9f3142366.png">

2. Save (Save to Playlist): <img width="1440" alt="Screenshot 2023-02-22 at 5 04 33 PM" src="https://user-images.githubusercontent.com/44684815/220559615-9cdea60c-be0e-4be7-9822-093f43e7f059.png">

3. Report: 

<img width="768" alt="Screenshot 2023-02-22 at 5 06 54 PM" src="https://user-images.githubusercontent.com/44684815/220559873-9b56a827-81e2-4808-8ec5-d93750df70c5.png">

--게다가 이런 <img width="35" alt="Screenshot 2023-02-22 at 5 07 43 PM" src="https://user-images.githubusercontent.com/44684815/220560026-25dc62be-eb25-46ef-85cc-a2154eec22f9.png"> 버튼을 누르면 ContextMenu가 나와서 Save, Share, Report를 보여준다.


***

## HoverVideoPlayer 기능

--Youtube sample website에서 마우스가 비디오보다 작은 그림들 위에 있다면 저절로 그림에 해당되는 비디오가 움직인다.



