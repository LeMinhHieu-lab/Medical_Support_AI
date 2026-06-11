# 🏥 Trợ Lý Y Tế Thông Minh (AI Medical Assistant)

Hệ thống trợ lý y tế thông minh được xây dựng bằng **LangGraph**, **LangChain** và **OpenAI GPT**, hỗ trợ tương tác với bệnh nhân thông qua hội thoại tự nhiên. Dự án cung cấp các chức năng như đặt lịch khám, quản lý hồ sơ bệnh nhân, phát hiện tình huống khẩn cấp và hỗ trợ tư vấn dựa trên ngữ cảnh hội thoại.

---

# 📌 Giới Thiệu

AI Medical Assistant là một hệ thống hội thoại y tế ứng dụng Mô hình Ngôn ngữ Lớn (LLM) kết hợp với kiến trúc điều phối luồng xử lý bằng LangGraph.

Hệ thống có khả năng:

* Đặt lịch và quản lý lịch khám bệnh
* Quản lý hồ sơ bệnh nhân
* Theo dõi tiền sử bệnh và dị ứng thuốc
* Phát hiện các trường hợp khẩn cấp
* Duy trì ngữ cảnh hội thoại nhiều lượt
* Hỗ trợ tư vấn y tế cơ bản

---

# 🚀 Tính Năng Chính

## 📅 Đặt Lịch Khám

* Hỗ trợ đặt lịch khám tự động
* Quản lý các cuộc hẹn tái khám
* Giao tiếp bằng ngôn ngữ tự nhiên

## 👤 Quản Lý Hồ Sơ Bệnh Nhân

* Lưu trữ thông tin bệnh nhân
* Quản lý tiền sử bệnh
* Theo dõi dị ứng thuốc
* Duy trì ngữ cảnh hội thoại

## 🚨 Phát Hiện Tình Huống Khẩn Cấp

* Nhận diện các triệu chứng nguy hiểm
* Cảnh báo người dùng khi phát hiện trường hợp khẩn cấp
* Hướng dẫn liên hệ cơ sở y tế hoặc dịch vụ cấp cứu

## 💬 Hội Thoại Có Ghi Nhớ Ngữ Cảnh

* Ghi nhớ các cuộc hội thoại trước đó
* Cá nhân hóa phản hồi
* Nâng cao trải nghiệm người dùng

## 🧠 Điều Phối Luồng Hội Thoại

* Phân loại ý định người dùng
* Định tuyến hội thoại theo từng tác vụ
* Xử lý ngữ cảnh bằng LangGraph

---

# 🏗️ Kiến Trúc Hệ Thống

```text
Người dùng
    │
    ▼
Bộ định tuyến hội thoại (LangGraph)
    │
    ├── Xử lý khẩn cấp
    │         │
    │         └── Cảnh báo và hướng dẫn
    │
    └── Xử lý AI
              │
              ├── Truy xuất hồ sơ bệnh nhân
              ├── Tạo ngữ cảnh
              ├── Sinh phản hồi bằng GPT
              └── Cập nhật bộ nhớ hội thoại
```

---

# ⚙️ Công Nghệ Sử Dụng

| Thành phần         | Công nghệ     |
| ------------------ | ------------- |
| Ngôn ngữ lập trình | Python        |
| Framework LLM      | LangChain     |
| Điều phối Workflow | LangGraph     |
| Mô hình AI         | OpenAI GPT    |
| Quản lý bộ nhớ     | InMemoryStore |
| Quản lý môi trường | Python Dotenv |

---

# 📂 Cấu Trúc Dự Án

```bash
medical-ai-assistant/
│
├── main.py
├── requirements.txt
├── .env.example
├── README.md
│
└── assets/
```

---

# 🔄 Quy Trình Hoạt Động

### Bước 1: Người dùng gửi yêu cầu

Người dùng nhập câu hỏi hoặc yêu cầu liên quan đến y tế.

### Bước 2: Phân tích ý định

Hệ thống xác định yêu cầu thuộc loại:

* Tình huống khẩn cấp
* Đặt lịch khám
* Tư vấn y tế thông thường

### Bước 3: Định tuyến hội thoại

LangGraph chuyển yêu cầu đến node xử lý phù hợp.

### Bước 4: Sinh phản hồi

OpenAI GPT tạo phản hồi dựa trên:

* Nội dung yêu cầu
* Hồ sơ bệnh nhân
* Lịch sử hội thoại

### Bước 5: Cập nhật bộ nhớ

Thông tin mới được lưu lại để phục vụ các cuộc hội thoại tiếp theo.

---

# 🛠️ Hướng Dẫn Cài Đặt

## Clone Dự Án

```bash
git clone https://github.com/<your-username>/medical-ai-assistant.git
cd medical-ai-assistant
```

## Cài Đặt Thư Viện

```bash
pip install -r requirements.txt
```

## Cấu Hình API Key

Tạo file `.env`

```env
OPENAI_API_KEY=your_api_key
```

## Chạy Ứng Dụng

```bash
python main.py
```

---

# 💡 Ví Dụ Hoạt Động

## Đặt Lịch Khám

```text
Người dùng:
Tôi muốn đặt lịch tái khám.

Hệ thống:
Tôi có thể hỗ trợ đặt lịch khám cho bạn.
Bạn muốn đặt lịch vào ngày nào?
```

## Tình Huống Khẩn Cấp

```text
Người dùng:
Tôi đang bị đau ngực dữ dội.

Hệ thống:
Phát hiện tình huống khẩn cấp.
Vui lòng liên hệ cơ sở y tế gần nhất hoặc gọi dịch vụ cấp cứu ngay lập tức.
```

---

# 📚 Kiến Thức Và Kỹ Thuật Được Áp Dụng

* Large Language Models (LLM)
* LangGraph Workflow
* LangChain
* AI Agent
* Conversational AI
* Prompt Engineering
* Context Engineering
* Memory-Augmented Chatbot
* Healthcare AI
* Stateful Conversation Management

---

# 🔮 Hướng Phát Triển Trong Tương Lai

* Tích hợp cơ sở dữ liệu lưu trữ lâu dài
* Áp dụng RAG (Retrieval-Augmented Generation)
* Kết nối hệ thống hồ sơ bệnh án điện tử (EHR)
* Hỗ trợ tương tác bằng giọng nói
* Tích hợp cơ sở tri thức y khoa
* Xây dựng hệ thống Multi-Agent
* Nâng cao bảo mật và quyền riêng tư dữ liệu


