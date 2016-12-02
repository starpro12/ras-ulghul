# ras-ulghul
라스-얼굴 프로젝트 [OpenFace](https://cmusatyalab.github.io/openface/) 기반으로 학습한 분류 모델에 대한 웹데모 프로젝트입니다.

자바진영의 spring-boot 프레임워크를 사용하여 만들었습니다.


## 설치하기
우선 프로젝트를 로컬로 clone합니다.
<pre><code>$ git clone https://github.com/socurites/ras-ulghul.git</code></pre>

웹 데모를 실행하기 전에 OpenFace 설치 위치, 학습된 모델 위치, 테스트할 이미지를 업로드할 위치 등을 변경합니다.
<pre><code>$ vi {RAS_ULGHUL_CLONED_DIRECTORY}/src/main/java/com/socurites/rasulghul/web/controller/RasUlGhulWebController.java</code></pre>

<pre><code>@Controller
public class RasUlGhulWebController {
  // OpenFace가 설치된 디렉토리
  private static final String OPEN_FACE_DIR = "/home/ubuntu/OpenFace/openface/";
  // 학습된 모델이 위치한 디렉토리의 prefix
  private static final String MODEL_DIR = "/home/ubuntu/artist_faces/model/generated-embeddings-";
  // 테스트할 이미지를 업로드할 위치
  // 반드시 {RAS_ULGHUL_CLONED_DIRECTORY}/src/main/webapp/resources/upload/로 설정한다.
  private static final String UPLOAD_DIR = "/home/ubuntu/git/ras-ulghul/src/main/webapp/resources/upload/";</pre></code>


