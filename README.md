# agentic-arch
통합 예제

**프로젝트를 열면서**
프로젝트 진행하며 AI를 많이 사용하게 되는데 뇌가 굳지 않도록 노력하는 것이 생각보다 중요합니다.
기억력 향상을 위한 [해결 방법 중 하나](https://www.youtube.com/watch?v=uXC7OuCas2Q)입니다.
지난 공백기에 개인 프로젝트를 진행하며 멘탈 관리와 사회성 유지에 체감이 되던 것은 운동 강도를 늘리고 알바, 봉사활동, 사교 활동으로 실제 사람과 상호작용하는 것이었습니다.
요리, 뜨개, 그 어떤 취미든 상관 없습니다.
SNS를 멀리하고 AI 도움 없이 작문하거나 책을 읽으며 AI 환경에 친숙해진 어휘력을 되찾아가는 것도 의미 있습니다.
AI를 도구로 사용한다고 해도 명령조, 반말, "~해줘" 식의 프롬프트는 지양해주세요.
웃음과 긴장감을 잃지 않도록 사람과의 상호작용이 있는 활동을 병행 하는 것을 추천 드립니다.

## Specification

Docker, Git, GitLab, Unix 기반 OS, Confluence, Java 25, Python 3.x, Spring 4.x, SpringAI, IntelliJ

> 문서 작성은 Trade-Off, Impact Scope 위주로 합니다.

- 미리 준비할 것: 완벽하지 않은 도메인 문서의 메타데이터를 스키마로 정리해두세요.
- 데이터 준비 시에 많은 양의 문서 처리가 중점인지, 답변의 정확도와 일관성이 중점인지, 문서 복잡성 해결인지 간단히 회의할 것.
- 구현하고 싶은 거, 도입해보고 싶은게 있다면 어필할 것.
- 도메인의 마일스톤 하나만 해결할 것.
- 규제가 있는 도메인은 데이터 거버넌스와 정책의 표준이 있다면 따를 것. 모르거나 없을 시에는 해당 데이터는 사용하지 않는다.
- 벤치마킹하거나 참고한 프로젝트 또는 기술은 꼭 표기할 것.

### Langchain 실습

> [공공 데이터](https://www.data.go.kr/) 파이프라인으로 sql agent 구현하기

- 카테고리 3개 이상 서로 겹치는 DB(만약 못 찾겠으면 민생쿠폰 업장 기준으로 DB 정규화 실습 해보세요. 복잡도는 상/중/하 로 나누자면 중간 정도입니다.)
- Langchain4j/Langchain
- VectorDB(QDrant/Milvus/PostgreSQL/chromaDB)
- Langfuse
- OpenAIAPI

혼자 진행해도 됩니다.
프롬프트 엔지니어링, Recall@10, Ragas, LLM as a Judge, BM25, 청킹, NER, DDD기반 도메인 파이프라인, LLM 가드레일, AI 보안 기술, Agent 오케스트레이션에 대해서 학습해오시면 좋습니다.
미디어 청킹 전략을 도입하고 싶다면 해보세요. 굳이 Sql Agent를 만들지 않아도 좋습니다.(Surya, OpenDataLoader 좋은 오픈소스가 많습니다.)
알고리즘 테스트 채점 기준의 Golden Set을 구성하고(예를 들자면 컴파일 처리 속도, 코드 난이도와 같은 것들) 평가해보는 Agent를 만드는 것도 방법입니다.
직접 구현한 Agent 성능을 측정할 때 구현해둔 Agent에 프롬프트 인젝션 공격과 방어를 해보는 것도 도움됩니다.
* ollama, gemma를 vllm로 학습시키고 실행해보세요. bedrock을 사용하고 싶다면 예제 구현하고 숫자로 모델 성능을 비교 해봐도 됩니다.

#### 난이도 조절

n8n으로 간단하게 매일하는 업무부터 langchain으로 자동화 해보세요.
[예제](https://youtu.be/4o0AJYBEiBo)와
잘 구현된 [MCP](https://mcp.aka.page/browse/quick)를 확인하는 것도 방법입니다.

### LlamaIndex/Langchain

> RAG 프레임워크 성능 비교

- LlamaIndex/Langchain
- VectorDB(QDrant/Milvus/PostgreSQL/chromaDB)
- Langfuse
- OpenAIAPI
- Streamlit

## 프로젝트 이전에 확인할 것

[Attention Is All You Need, BERT의 시작](https://arxiv.org/abs/1706.03762)
[Auto Ontology, 온톨로지 레이어 구축 이해](https://github.com/NVIDIA/auto-ontology)
[왜 메타데이터와 온톨로지 방식으로 해결해야 되는지](https://github.com/NVIDIA/auto-ontology-eval)
[Graph-R1, GraphRAG에 대한 이해](https://arxiv.org/html/2507.21892v2)
[Coherence 해결](https://arxiv.org/html/2508.07975v1)
[왜 LlamaIndex여야 되는가?](https://blog.abdellatif.io/production-rag-processing-5m-documents)
[왜 LangChain이어야 되는가?](https://www.youtube.com/watch?v=VoWGD4mvKjU)
[RAG](https://www.promptingguide.ai/kr/research/rag)
[AWS RAG 서비스](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html)
[간단한 RAG 구현기](https://tech.ktcloud.com/entry/2025-02-ktcloud-ai-rag-faiss-%EA%B0%9C%EB%B0%9C%EB%B0%A9%EC%8B%9D-%EA%B5%AC%ED%98%84)
[SpringAI](https://youtu.be/x6KmUyPWy2Q)
[pytorchKR](https://discuss.pytorch.kr/)
