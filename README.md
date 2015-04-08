### 프로젝트 ###
twitcurl을 이해하고 분석하기 위한 fork 프로젝트입니다.


### 소개: ###
**twitcurl** 은 트위터 API를 지원하는 순수 C++ 라이브러리입니다. cURL을 사용해 HTTP Request와 Response를 핸들링합니다. 윈도우, 우분투, 데비안에서 테스트 되었으며, cURL을 지원하는 모든 운영체제에서 잘 동작할 것입니다.
  * v1.1 Twitter REST APIs
  * JSON
  * SSL

### OAuth ###
**twitcurl** 은 OAuth 인증 메소드들을 지원합니다. **trunk** 섹션의 **twitterClient** 예제 코드를 통해 twitcurl OAuth의 순서를 알 수 있습니다 자세한 정보는 다음 페이지를 참고하세요: http://code.google.com/p/twitcurl/wiki/TwitcurlOAuthFlow


### APIs ###
현재 twitcurl은 다음과 같은 트위터 REST API들의 래퍼 함수를 가지고 있습니다:<br>
<b>타임라인 메소드:</b><br>
statuses/public_timeline<br>
statuses/friends_timeline<br>
statuses/user_timeline<br>
statuses/mentions<br>

<b>상태 메소드:</b><br>
statuses/show<br>
statuses/update<br>
statuses/destroy<br>

<b>유저 메소드:</b><br>
users/show<br>
statuses/friends<br>
statuses/followers<br>

<b>DM 메소드:</b><br>
direct_messages<br>
direct_messages/sent<br>
direct_messages/new<br>
direct_messages/destroy<br>

<b>친구 메소드:</b><br>
friendships/create<br>
friendships/destroy<br>
friendships/show<br>

<b>소셜 그래프 메소드:</b><br>
friends/ids<br>
followers/ids<br>

<b>계정 메소드:</b><br>
account/rate_limit_status<br>

<b>관심글 메소드:</b><br>
favorites<br>
favorites/create<br>
favorites/destroy<br>

<b>차단 메소드:</b><br>
blocks/create<br>
blocks/destroy<br>
blocks/list<br>
blocks/ids<br>

<b>저장된 검색 메소드:</b><br>
saved_searches<br>
saved_searches/show<br>
saved_searches/create<br>
saved_searches/destroy<br>

<b>트렌드 메소드:</b><br>
trends<br>
trends/current<br>
trends/daily<br>
trends/weekly<br>
trends/available<br>

<h3>소스:</h3>
<ul><li>twitcurl 소스는 "Source" 탭의 리포지토리에서 사용이 가능합니다.<br>
</li><li>윈도우에서 빌드할 수 있는 Microsoft Visual C++ 6.0 및 2008용 워크스페이스와 UNIX/LINUX 컴포넌트에서 사용할 수 있는 Makefile이 포함되어 있습니다.<br>
</li><li>TortoiseSVN과 같은 SVN이나 툴을 사용해 (<a href='http://tortoisesvn.net/'>http://tortoisesvn.net/</a>) 파일을 다운로드하고 체크아웃합니다.</li></ul>


<h3>도움이 필요하신가요?</h3>
twitcurl 라이브러리를 빌드하고 사용하는 자세한 정보를 위키 섹션에서확인하세요.<br>
<a href='http://code.google.com/p/twitcurl/wiki/WikiHowToUseTwitcurlLibrary'>http://code.google.com/p/twitcurl/wiki/WikiHowToUseTwitcurlLibrary</a>


<h3>메모:</h3>
<ul><li>twitcurl returns JSON responses from twitter.com as it is. You need to have a JSON parser to parse the responses.<br>
</li><li>twitcurl uses HMAC_SHA1  from <a href='http://www.codeproject.com/KB/recipes/HMACSHA1class.aspx'>http://www.codeproject.com/KB/recipes/HMACSHA1class.aspx</a>
</li><li>twitcurl uses base64 from <a href='http://www.adp-gmbh.ch/cpp/common/base64.html'>http://www.adp-gmbh.ch/cpp/common/base64.html</a>
</li><li>Check out <a href='http://www.json.org/'>http://www.json.org/</a> for C/C++ parsers.</li></ul>


<h3>예제:</h3>
twitcurl을 동적 라이브러리로 사용하는 예제 트위터 클라이언트 프로그램은 "Downloads" 섹션에서 이용이 가능합니다.<br>
<br>
<br>
<h3>정보:</h3>
<ul><li>cURL에 대한 자세한 정보는 여기서 확인: <a href='http://curl.haxx.se/'>http://curl.haxx.se/</a>
</li><li>트위터 REST API들에 대한 자세한 정보는 여기서 확인: <a href='http://apiwiki.twitter.com/w/page/22554679/Twitter-API-Documentation'>http://apiwiki.twitter.com/w/page/22554679/Twitter-API-Documentation</a>
</li><li>트위터 OAuth 인증에 대한 자세한 정보는 여기서 확인:<br>
<ul><li><a href='http://dev.twitter.com/auth'>http://dev.twitter.com/auth</a>
</li><li><a href='http://www.jaanuskase.com/en/2010/01/understanding_the_guts_of_twit.html'>http://www.jaanuskase.com/en/2010/01/understanding_the_guts_of_twit.html</a>
</li><li><a href='http://codebrook.wordpress.com/2010/07/08/twitter-oauth-in-cpp-for-win32/'>http://codebrook.wordpress.com/2010/07/08/twitter-oauth-in-cpp-for-win32/</a>
</li></ul></li><li>Building cURL static library with SSL on Windows: <a href='http://swatrant.blogspot.in/2013/06/how-to-build-curl-static-library-with.html'>http://swatrant.blogspot.in/2013/06/how-to-build-curl-static-library-with.html</a>
