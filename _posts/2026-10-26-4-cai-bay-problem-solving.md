---
title: '4 cái bẫy Problem Solving phổ biến của PM trẻ'
description: "Đừng nhầm lẫn giữa giải pháp user đòi hỏi và vấn đề họ thực sự gặp phải. Bài viết đúc kết 4 cạm bẫy tư duy từ các case study thực tế khi xây dựng sản phẩm"
author: Trung Nguyễn
date: 2026-10-26 21:28:00 +0700
categories: [Product Management, Strategy, Work, Career]
tags: [product-management, problem-solving, product-mindset, zalo]
comments: true
image:
  path: /assets/img/posts/4_cai_bay_problem_solving/banner.jpg
---

Gần đây, mình có dịp ngồi hội đồng chấm điểm các dự án Product Management Trainee (PMT) ở Zalo, cộng với việc trước giờ mình dành khá nhiều thời gian làm việc cùng các bạn Product trẻ, mình nhận ra một số pattern chung trong cách các bạn tư duy và tiếp cận vấn đề.
Bài này, mình sẽ phân tích lại một số điểm đó, đi kèm với những case study "xương máu" mà cá nhân mình từng trải qua, và đề xuất hướng cải thiện.

> **Disclaimer:** Đây là đúc kết từ quan sát cá nhân của mình, không phải công thức tuyệt đối. Mình có một câu nói rất tâm đắc: "Good PM = Good Problem Manager" – vì thế với mình việc cải thiện được kỹ năng Problem Solving sẽ giúp ích rất nhiều cho mọi người trong việc xây dựng sản phẩm
{: .prompt-info }

<div class="tldr-box" markdown="1"> 
**TL;DR:**
1. Đừng nhảy ngay vào giải pháp, hãy đào sâu tìm *painpoint* thực sự của user (vì user hay đưa cho bạn giải pháp họ tự nghĩ ra - user want >< user need).
2. Thu thập vấn đề xong phải validate và định lượng nó (Who, Usage, Critical, Scope) để có cơ sở sắp xếp ưu tiên, resource.
3. Vẽ rõ chân dung Target Audience. Việc sẵn sàng quyết định mình KHÔNG phục vụ ai cũng là một quyết định sắc bén.
4. Hãy cố gắn align tính năng mình làm với mục tiêu chung của phòng ban, và đo đạc được impact rõ ràng. Đừng mang "Task" ra làm "KPI". Phân biệt rõ 3 tầng LV1 (Shipped) - LV2 (Used) - LV3 (Changed).
</div>

---
### 1. Nhảy ngay vào giải pháp trước khi thật sự hiểu được vấn đề

Một quán tính phổ biến mình hay thấy là các bạn trẻ thường nhầm lẫn giữa **những thứ user đề xuất** và **vấn đề (painpoint) thật sự đằng sau của họ**. Điều này rất dễ dẫn tới việc các bạn cắm đầu vào làm solution, bị lái theo cái user "muốn" chứ không phải cái họ thật sự "cần".

**Câu chuyện 1: Group Channel vs. Pinned Message**
Giai đoạn còn làm mảng Group Communication, mình nhận được rất nhiều feedback kiểu: *"Tôi muốn Zalo có tính năng Group Channel giống Telegram"* hay *"Cho tôi setting quyền cấm tất cả member chat trong nhóm"*.
Nhu cầu tạo channel 1 chiều (như các hội nhóm Coin, News... trên Telegram) lúc đó đang rất trend. Nếu lao vào làm ngay theo giải pháp user gợi ý, tụi mình sẽ phải đẻ ra một concept group mới, đồng bộ server, làm UX flow riêng, disable chat, chặn chia sẻ, onboard - promote cho user... ==> Chi phí bỏ ra cực kì khổng lồ.

Nhưng khi mình cho đào sâu hơn, painpoint thực sự của user chỉ là: *họ không muốn các tin thông báo quan trọng trong group bị trôi do member khác nhắn xen vào*, nên họ mới đề xuất hay là cấm chat tất cả thành viên.
Khi bóc tách được vấn đề lõi: *"Làm sao để tin nhắn quan trọng không bị trôi?"*, team mình chuyển hướng ra mắt tính năng optimize Pin Message (ghim nhiều tin nhắn hơn) và promote hướng dẫn cho các admin. Cost giảm đi đáng kể, mà lại gãi đúng ngay chỗ ngứa của user.

**Câu chuyện 2: Cái nút Copy ảnh trên Zalo PC**
Hồi mình làm Zalo PC, thi thoảng có nhận vài request kiểu: *"Anh chọn nhiều ảnh mà bấm copy không được"*. Mình check lại thì đúng là bản PC đang thiếu tính năng copy nhiều ảnh. Thật ra, nếu nhảy vào support luôn cái nút Copy thì cost cũng chẳng nhiều gì. Tuy nhiên, mình vẫn quyết định reach user để hiểu rõ use-case của họ. Hóa ra, đây là các bạn shipper, sale muốn copy ảnh để gửi cho khách (người lạ) mà không cần phải kết bạn. Vấn đề lúc này được frame lại thành: *"Làm sao để forward ảnh, tin nhắn tới người lạ nhanh/tiện nhất?"*. 
* Nếu làm theo luồng cũ (thêm nút Copy): Chọn nhiều ảnh -> Copy -> Tìm chat người lạ -> Paste -> Gửi (Mất 5 steps).
* Giải pháp team mình quyết định làm: Support ngay cho ở màn hình chia sẻ hiển thị thêm người lạ. Chọn nhiều ảnh -> Bấm Forward -> Chọn người lạ -> Gửi (Chỉ 4 steps).

==> Vậy nên, xác định đúng vấn đề cực kì quan trọng, nó nên chiếm phần lớn thời gian ban đầu. Ở Zalo, tụi mình chắt lọc vấn đề từ:
*   **User voice:** User Survey (Quanti) & User Interview (Quali), App Store Review...
*   **Data:** Stats, Funnel, Wordcloud, A/B Testing Results.
*   **Market & Competitors Review.**
*   Và **Product sense:** Kinh nghiệm của chính mình khi đặt bản thân vào lăng kính user.

### 2. Thu thập nhiều vấn đề, nhưng chưa validate và định lượng Problem

Một sai lầm tiếp theo: Phỏng vấn user xong, cào data xong, các bạn mang về một danh sách dài dằng dặc các vấn đề rồi... hăm hở nhảy vào làm solution. Cái bẫy ở đây là các bạn chưa thật sự validate nó, không định lượng được đây là vấn đề lớn hay nhỏ, impact ra sao. 

Ví dụ team mình từng đứng trước 2 luồng feedback cùng thời điểm như thế này:
1. Tool Storage sau khi update UI 4.0 bị đơ, load mất tới 30s
2. Lỗi UX của My Cloud khiến user confuse không biết thêm ảnh vào như thế nào

Resource thì có hạn, ưu tiên làm cái nào trước? Lúc này phải lôi số ra nói chuyện: Vấn đề (1) ảnh hưởng tới khoảng 2.4M user (tập A30), trong khi vấn đề (2) ảnh hưởng tới >10M user. Thế là mình nên ưu tiên vấn đề (2) vì nó impact tới nhiều user hơn chăng?
Thực tế là, dù vấn đề đầu tiên ảnh hưởng đến ít người dùng hơn, nhưng mức độ nghiêm trọng lại cao hơn hẳn khiến họ không thể sử dụng ứng dụng và dễ dàng rời bỏ flow ngay từ đầu (không còn bao nhiêu user kiên nhẫn đợi load tận 30s cả). Trong khi đó, vấn đề thứ hai tuy tác động rộng hơn nhưng người dùng vẫn có cách workaround tạm thời. Do đó, chúng ta cần ưu tiên giải quyết vấn đề thứ nhất hơn

Hay 1 ví dụ khác, đu theo trend hiện tại: Việc "khảo sát hiến tạng trẻ em" liệu có phải vấn đề critical và có tỷ lệ cao đến mức phải ưu tiên giải quyết ngay so với hàng loạt vấn đề y tế nhức nhối khác không (quá tải ở bệnh viện, thiếu trang bị y tế ...)?

**Hướng giải quyết:**
Đừng chỉ liệt kê. Hãy Validate bằng 4 keyword:
*   **Who:** Target là ai? Phân khúc nào? (Số lượng user bị phải là con số tuyệt đối, đừng chỉ đưa %)
*   **Usage:** Tần suất gặp lỗi. (Một tập nhỏ ngày nào cũng bị, hay tập lớn lâu lâu mới bị?)
*   **Critical:** Có đụng tới core values không? (Đôi khi lỗi ít người gặp nhưng dính tới privacy - core value của sản phẩm chẳng hạn, hoặc một con bug minor gây cảm giác thiếu chuyên nghiệp thì vẫn là vấn đề cần ưu tiên ; hoặc như ví dụ trên chẳng hạn)
*   **Scope:** Có thuộc scope mình giải quyết không? Lấy ví dụ khi giải quyết bài toán spam add nhóm (scope Communication): Triệu chứng là người dùng liên tục bị làm phiền bởi những nhóm chat lạ từ các mối quan hệ đã quên. Tuy nhiên, nguyên nhân gốc rễ lại không nằm ở tính năng chat hay nhóm, mà bắt nguồn từ cơ chế kết bạn ngày xưa quá dễ dãi thuộc scope Core

### 3. Không hiểu rõ Target Audience (Bẫy "Build for everyone")

Không hiểu rõ Target Audience là một bẫy cực kỳ phổ biến. Mình thấy rất nhiều bạn PM trẻ khi nhận diện được một vấn đề là lập tức muốn làm ra một tính năng giải quyết cho "tất cả mọi người". Nhưng sự thật phũ phàng trong làm Product là: **Sản phẩm làm cho tất cả mọi người, cuối cùng sẽ chẳng ai dùng cả**.

Mọi người thường chỉ raise được vấn đề chung chung, nhưng lại không thực sự bóc tách được mình **đang phục vụ ai là chính**. Nếu không biết mình phục vụ ai, bạn sẽ gặp vô vàn khó khăn:
*   **Lựa chọn sai giải pháp:** Cùng một nỗi đau, nhưng cách tiếp cận và xử lý cho từng đối tượng là hoàn toàn khác nhau. Nếu bạn gom chung, bạn sẽ tạo ra một tính năng nửa vời, không hoàn toàn fit với 1 bên nào cả
*   **Sai lầm khi Release & Promote:** Khi ra mắt tính năng, bạn sẽ không biết chọn đúng tập để truyền thông, promote. Dẫn tới rủi ro đi spam thông báo cho cả những người không có nhu cầu, gây phiền toái và ảnh hưởng tới trải nghiệm chung

**Ví dụ 1: Bài toán đồng bộ tin nhắn**
Đối với bài toán đồng bộ tin nhắn từ Mobile lên PC, tập user mục tiêu thực sự không phải là 100% user Zalo, mà là *"Multi-device users"* (Người dùng đa thiết bị, dân văn phòng, sale...). Nếu bạn không khoanh vùng được tập này, bạn có thể vô tình ép luồng onboarding phức tạp hoặc push noti promote tính năng đồng bộ lên cả tệp các cô chú lớn tuổi – những người chỉ chỉ có đúng 1 nhu cầu xài Zalo để gọi video cho con cháu (với tập này, giá trị lớn nhất của họ là sự ĐƠN GIẢN, DỄ SỬ DỤNG của Zalo)

**Ví dụ 2: Bài toán "Zalo chiếm nhiều dung lượng"**
Đây là một painpoint rất phổ biến. Nhưng nếu bạn nhảy vào làm giải pháp ngay mà không mổ xẻ Target Audience, bạn sẽ bị kẹt. Thực tế, cùng một vấn đề "hết dung lượng", nhưng chúng ta có 2 tệp user với nhu cầu hoàn toàn trái ngược:
*   *Tệp A (Người lớn tuổi, xài máy phổ thông dung lượng ít 32GB):* Nỗi đau của họ là máy hay bị đơ, không chụp ảnh được nữa. Giải pháp họ cần cực kì đơn giản: Một cách nào "Dọn dẹp nhanh" để giải phóng bộ nhớ, không phải nghĩ ngợi nhiều.
*   *Tệp B (Dân văn phòng, xài máy 256GB+):* Nỗi đau của họ là sợ bị mất file công việc, không tìm lại được tài liệu cũ sau 1 tháng. Giải pháp họ cần là cho phép lưu trữ file lâu dài, không bị mất nhưng không chiếm nhiều dung lượng (offload nhưng vẫn giữ trên cloud)
=> Nếu bạn không chia rõ 2 tập Audience này, bạn có thể sẽ bắt người lớn tuổi đi học xài Cloud, offload ..., hoặc cung cấp cho dân văn phòng một cái nút xóa file bừa bãi, gây mất dữ liệu quan trọng. Cả 2 đều sẽ là thảm họa.

**Hướng giải quyết:**
1.  **Vẽ rõ Context (Ngữ cảnh) qua framework JTBD:** Đừng chỉ dừng lại ở Demographic (độ tuổi, giới tính). Hãy đặt họ vào **Jobs-to-be-Done**: *"Khi [ngữ cảnh], Tôi muốn [hành động], Để tôi có thể [kết quả mong đợi]"*. (VD: Khi đang soạn chat dở trên điện thoại, tôi muốn mở PC lên là có sẵn draft tin nhắn, để tôi có thể tiếp tục làm việc tiếp ngay lập tức mà không phải gõ lại).
2.  **Cắt lát Data (Data Segmentation):** Đừng nhìn số tổng. Hãy bóc tách data để xem tập user đang chịu nỗi đau này chiếm bao nhiêu phần trăm? Hành vi của họ có gì đặc thù?
3.  **Dám nói "Không":** Đôi khi, sau khi xác định rõ ràng tập Target Audience của mình rồi, việc đưa ra quyết định **MÌNH KHÔNG PHỤC VỤ TẬP KIA** cũng là một lựa chọn chiến lược cực kỳ quan trọng và dũng cảm của một PM.

### 4. Không kết nối được với direction chung (Top-down)

Một trong những câu hỏi mình hay hỏi xoáy các bạn nhất khi bảo vệ dự án là: *"Tính năng của em đóng góp thế nào vào mục tiêu chung (OKR/Direction) của team trong quý/năm này?"*. 1 câu hỏi để vừa đánh giá xem bạn có nắm rõ được mục tiêu chung hay không, và xác định cách đánh giá impact như thế nào

Mình thấy các bạn hay bênh vực dự án của mình một cách rất cục bộ, tự hào bằng **Output** (VD: *Em ra mắt tính năng X kịp deadline, tỷ lệ user ban đầu xài khá tốt ...*) thay vì **Outcome** thật sự (*Vấn đề được giải quyết, Revenue tăng, Retention tăng*).

Để dễ hiểu, mình thường đưa ra bức tranh 3 tầng (3 Tiers) để map mọi thứ lại:
*   **LV1 (Shipped):** What WE do. Ra mắt được tính năng, release được xx features, có bao nhiêu tin nhắn, campaigns được chạy ...
*   **LV2 (Used) - Objective-KR:** USER behavior - là những signal ban đầu cho thấy tính user sử dụng tính năng như thế nào: click, open, usage, adoption...
*   **LV3 (Changed) - KPI/Outcome:** The REAL CHANGE mà chúng ta muốn hướng tới
Output = LV1 + LV2 (what we ship & what gets used). Outcome = LV3 (what actually changes)

VD: 
- Mục tiêu là giảm cân, LV1 = mua gói gym 12 tháng, mua vé tháng bơi; LV2 = tập 3 buổi 1 tuần, đốt 500kcal 1 buổi; LV3 = Vòng bụng giảm được 5cm, chỉ số mỡ máu giảm về mức bình thường, giảm được 5kg
- Học anh văn bằng duolingo: LV1 = cài app, mua sub; LV1 = 200-day streak (đây là 1 cái bẫy mà các app hay khai thác, để keep motivation của mình), nhưng thực tế cái outcome mình muốn hướng tới LV3 = thật sự pass 1 cuộc phỏng vấn = tiếng anh, hoặc mình conduct 1 meeting hoàn toàn bằng tiếng anh
1 VD khác về sản phẩm:
- Bài toán mất dữ liệu của Zalo: LV1: release tính năng auto download (download ngầm toàn bộ dữ liệu về local cho user không bị mất), LV2: tỉ lệ auto download thành công lên tới 99%. Tuy nhiên đây là 1 cái bẫy, đa phần các bạn PM sẽ thường lấy chỉ số LV2 để đánh giá impact, nhưng thực sự việc auto download đủ có thể hiện được user không còn mất dữ liệu nữa hay không => câu trả lời là KHÔNG, vẫn còn nhiều trường hợp như user đổi máy, user xóa dữ liệu manual ... => vì thế để đo được outcome thật sự đánh giá bài toán mất dữ liệu của Zalo thì phải thể hiện qua chỉ số LV3 = Tỉ lệ user thấy resources media bị roll trên Zalo (%) => đây mới thật sự là chỉ số outcome cuối cùng mình muốn hướng tới.

*Rút ra*
- Hãy bắt đầu từ KPI (LV3) và tự vấn ngược lại hành vi nào của người dùng cần thay đổi (LV2 - KR), thay vì vội vàng nghĩ đến việc làm tính năng gì (LV1 - Task). Cần nhớ rằng "ship feature" hay hoàn thành đầu việc chỉ là điểm khởi đầu, tuyệt đối không được nhầm lẫn nó với impact thật sự.
- Khi bạn chứng minh được giải pháp của mình "align" chặt chẽ từ LV1 lên LV3, bạn sẽ dễ dàng leverage sự ưu tiên để mượn resource và phối hợp nhịp nhàng với các bên cũng như chứng minh được impact của sản phẩm của mình vừa tạo ra.
---

### Lời kết

Mình luôn tin rằng, một bản solution proposal xuất sắc không nằm ở việc nó giải quyết được bao nhiêu tính năng, mà nằm ở việc nó tập trung **xử lý dứt điểm đúng một nỗi đau**.
Vì thế, đừng jump ngay vào giải pháp. Hãy dành thời gian suy nghĩ thấu đáo vấn đề, validate và quantify nó để ưu tiên resource cho hợp lý. Hiểu rõ mình đang phục vụ ai, và quan trọng là, phải kết nối impact của giải pháp với mục tiêu chung.