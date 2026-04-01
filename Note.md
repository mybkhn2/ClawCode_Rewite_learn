Claw Code — Rewrite
law Code — Rewrite của Claude Code đang gây bão cộng đồng AI!
Lúc 4 giờ sáng ngày 31/3/2026, source code của Claude Code bị lộ ra ngoài. Và chỉ trong vài giờ, một kỹ sư tên Sigrid Jin đã ngồi port lại toàn bộ từ đầu bằng Python — trước khi mặt trời mọc.
Kết quả? Repo claw-code phá kỷ lục: đạt 50.000 ⭐ trong vòng 2 tiếng sau khi publish — nhanh nhất lịch sử GitHub.
📌 Dự án này là gì?
→ Một bản rewrite sạch hoàn toàn bằng Python, tái tạo kiến trúc harness của Claude Code mà không copy code gốc
→ Đang được port sang Rust để chạy nhanh hơn, memory-safe hơn
→ Toàn bộ quá trình porting được orchestrate bởi AI (oh-my-codex + OpenAI Codex)
🗞️ Sigrid Jin còn được Wall Street Journal phỏng vấn — người đã sử dụng 25 tỷ token Claude Code chỉ trong một năm.
Đây là minh chứng rõ ràng nhất cho thấy AI đang tự viết lại các công cụ AI — và cộng đồng đang di chuyển nhanh hơn bất kỳ tổ chức nào.
🔗 https://github.com/autobytaste-lab/claw-code

iải thích thêm cho anh em hiểu tại sao nó hot ?
1) Bản chất: đây là một kiểu agentic tool (giống như OpenClaw/ Claude Code / hay các Agentic coding tool khác)
2) Bộ não: dĩ nhiên là vẫn dùng các model AI phía sau để làm bộ não xử lý các request của mình rồi, cái này ai cũng hiểu, chúng ta trả tiền là trả cho phần bộ não là chính yếu.
3) Tool call: đây mới là điểm mấu chốt, trước đây mình cũng không hiểu, vô tình đọc được bài viết của một bác nào đó trên facebook giải thích mình mới hiểu rõ, hóa ra, việc bạn yêu cầu bộ não phân tích rồi làm này làm kia...Bản thân các model AI nó không thể gọi trực tiếp tool (gọi command) trên máy tính của bạn được. Mà nó sẽ trả về kết quả output gì đó, các công cụ agentic phải parse dữ liệu đó rồi tạo thành dòng lệnh (command, chạy theo OS cho phù hợp) sau đó sẽ cần xin quyền của user để thực thi. Về việc parse tool này thì kha khá nặng nhọc, ví dụ như parse output từ model để tạo command xóa file trên Windows/Linux/MacOS. Phê cực kì.
4) Skills và Plugins: ví dụ như agent swarm dĩ nhiên rồi, team của Claude Code đã làm việc liên tục để bổ sung thêm mấy thứ hay ho này.
Sơ bộ thì mọi người có thể thấy, thằng OpenClaw cũng được build như vậy, họ bổ sung cho nó rất nhiều skills/ Plugins/ tool call để nó có thể hoạt động tốt trên các OS. Chỉ cần lắp bộ não vào cho nó là được.