# Báo Cáo Nhóm Day 24 Track 1

## So Sánh Risk Profile Giữa Các Ngành AI

Phần nhóm này tổng hợp 3 bài cá nhân đã được cung cấp và đối chiếu với yêu cầu lab về so sánh `risk profile` giữa các ngành.

## 1. Thành Viên Và Ngành Phụ Trách

| Thành viên | Ngành phụ trách | File đầu vào |
|---|---|---|
| Võ Tấn Trung | Media / News / Social / Political assistant | `VoTanTrung-report.md` |
| Nguyễn Hoàng Thanh Tùng | Giáo dục / AI Tutor | `NguyenHoangThanhTung-report.md` |
| Nguyễn Minh Đức | Mobility / autonomous driving | `NguyenMinhDuc-report.md` |

Nhóm hiện có dữ liệu từ 3 ngành. Các ngành `HR / tuyển dụng`, `Y tế / symptom checker / health assistant` và `Content creator` nằm trong danh sách lab nhưng không có bài cá nhân trong 3 file đầu vào, nên báo cáo không tự tạo thêm case mới cho các ngành này.

## 2. Đối Chiếu Với Yêu Cầu Phần Nhóm

| Yêu cầu nhóm trong lab | Cách báo cáo đáp ứng |
|---|---|
| Share toàn bộ 2-3 case của mỗi thành viên | Báo cáo tổng hợp 9 case từ 3 bài cá nhân. |
| Có bảng so sánh các ngành | Mục 4 có bảng so sánh theo các cột: ngành, harm dễ gặp nhất, `failure mode`, `layer`, `risk profile`, và lý do. |
| Có đoạn tổng hợp ngắn về `risk profile` giữa các ngành | Mục 5, 6 và 7 trình bày phân tích liên ngành, trả lời câu hỏi thảo luận và kết luận nhóm. |

## 3. Dữ Liệu Đầu Vào Từ Các Bài Cá Nhân

| Ngành | Case đã phân tích | Số liệu nổi bật | Pattern rủi ro trong ngành |
|---|---|---|---|
| Media / News / Social / Political assistant | Google AI Overviews 2024; Perplexity AI 2024; CNET AI-generated articles 2022-2023 | Khoảng 10% người dùng toàn cầu bắt đầu dùng chatbot AI để đọc tin tức; chỉ 20% tin tưởng bot AI về tin tức; CNET có 77 bài viết AI, hơn một nửa bị phát hiện lỗi và khoảng 41 bài phải đính chính. | Hallucination, misinformation, trích dẫn sai hoặc thiếu, vi phạm bản quyền, đạo văn và suy giảm niềm tin vào báo chí. |
| Giáo dục / AI Tutor | Ofqual grading algorithm 2020; Stanford GPT detector bias 2023; PNAS AI Tutor study 2025 | Ofqual: gần 36% điểm A-level bị hạ một bậc; 15.000 học sinh ban đầu bị trường đại học nguyện vọng một từ chối; hơn 4,6 triệu điểm GCSE bị tác động. Stanford: false positive với bài TOEFL của người viết phi bản xứ lên tới 61,22%. PNAS: GPT Base làm điểm thi độc lập giảm 17% so với nhóm đối chứng. | Bias / fairness, opportunity loss, dignity loss, over-reliance, suy giảm năng lực học thật và xử lý dữ liệu học tập nhạy cảm. |
| Mobility / autonomous driving | Uber self-driving fatal crash 2018; Cruise robotaxi pedestrian dragging 2023; Tesla Autopilot / Autosteer recall 2023 | Uber: hệ thống phát hiện người đi bộ khoảng 5,6 giây trước va chạm và vụ việc gây 1 ca tử vong. Cruise: recall 950 xe sau vụ kéo lê người đi bộ. Tesla: recall hơn 2 triệu xe tại Mỹ. | Lỗi nhận diện/dự đoán, hành vi sau va chạm, `escalation failure`, `over-reliance` và nguy cơ harm vật lý. |

### 3.1. Phân Tích Chi Tiết Theo Từng Thành Viên

**Võ Tấn Trung - Media / News / Social / Political assistant.** Phần phân tích của Võ Tấn Trung cho thấy rủi ro trong ngành tin tức AI chủ yếu nằm ở chuỗi thu thập, tổng hợp và dẫn nguồn. Google AI Overviews thể hiện rủi ro hallucination khi hệ thống tạo câu trả lời nghe có vẻ chắc chắn nhưng sai về nội dung. Perplexity AI thể hiện rủi ro bản quyền và trích dẫn khi một công cụ trả lời tin tức có thể tóm tắt hoặc tái sử dụng nội dung báo chí mà không tạo đủ giá trị truy cập ngược cho nhà xuất bản. CNET cho thấy khi AI được dùng để viết bài trong lĩnh vực tài chính cá nhân, lỗi tính toán hoặc diễn giải sai có thể làm người đọc ra quyết định sai. Điểm chung của ngành này là harm không nhất thiết gây chấn thương trực tiếp, nhưng có thể làm méo nhận thức công chúng, làm suy giảm niềm tin vào báo chí và tạo thiệt hại kinh tế cho nhà xuất bản.

**Nguyễn Hoàng Thanh Tùng - Giáo dục / AI Tutor.** Phần phân tích của Nguyễn Hoàng Thanh Tùng cho thấy AI trong giáo dục có rủi ro cao vì chạm trực tiếp đến cơ hội học tập, đánh giá năng lực và danh dự học thuật. Case Ofqual là ví dụ rõ nhất về nguy cơ dùng mô hình thống kê để thay thế phán đoán cá nhân trong một kỳ thi quốc gia: thuật toán không chỉ sai ở cấp cá nhân mà còn tạo bất công hệ thống giữa các nhóm trường học. Case Stanford GPT detector bias cho thấy một công cụ có vẻ trung lập vẫn có thể trừng phạt nhóm người viết tiếng Anh phi bản xứ do đặc điểm ngôn ngữ của họ bị mô hình hiểu nhầm là dấu hiệu của AI. Case PNAS AI Tutor cho thấy nếu AI Tutor đưa lời giải trực tiếp mà không có rào chắn sư phạm, học sinh có thể làm bài tốt hơn khi có AI nhưng học thật kém hơn khi kiểm tra độc lập.

**Nguyễn Minh Đức - Mobility / autonomous driving.** Phần phân tích của Nguyễn Minh Đức cho thấy Mobility là ngành có mức harm vật lý rõ nhất. Case Uber Tempe 2018 cho thấy một chuỗi lỗi nhận diện, phản ứng và chuyển giao trách nhiệm có thể dẫn đến tử vong. Case Cruise San Francisco 2023 nhấn mạnh rủi ro sau va chạm: xe tự lái không chỉ cần tránh va chạm mà còn phải biết dừng an toàn khi tình huống đã trở nên bất thường. Case Tesla Autopilot / Autosteer cho thấy ngay cả hệ thống hỗ trợ lái cấp độ 2 cũng có thể tạo rủi ro lớn nếu người lái hiểu nhầm năng lực tự động hóa và giảm chú ý. Điểm chung của ngành này là thời gian phản ứng rất ngắn, môi trường vận hành phức tạp và hậu quả sai sót thường khó đảo ngược.

## 4. Bảng So Sánh Risk Profile Giữa Các Ngành

| Ngành | Harm dễ gặp nhất | Failure mode hay lặp lại | Layer hay bắt đầu lỗi | Risk profile tổng thể | Vì sao? |
|---|---|---|---|---|---|
| Media / News / Social / Political assistant | Misinformation, hallucination, trích dẫn sai, vi phạm bản quyền, mất niềm tin công chúng và làm suy yếu hệ sinh thái báo chí. | Hallucination, fake / missing citation, copyright misuse, plagiarism, lựa chọn nguồn thiên lệch. | Retrieval, LLM Generation, Citation Selection, Safety Filters. | High | Severity thường không trực tiếp gây hại vật lý, nhưng Scale và Frequency cao vì nội dung tin tức có thể lan rộng nhanh, đặc biệt trong chính trị, y tế và tài chính. |
| Giáo dục / AI Tutor | Opportunity loss, dignity loss, privacy loss, unfair scoring, cáo buộc gian lận oan và suy giảm năng lực học thật. | Bias / fairness, over-reliance, harmful advice, weak pedagogical guardrails, proxy-based scoring. | Model, Safety, UX, Data Governance. | Critical | AI có thể ảnh hưởng trực tiếp đến điểm số, tuyển sinh, kỷ luật học thuật và dữ liệu nhạy cảm của người học. Case Ofqual cho thấy tác động cấp quốc gia; case Stanford cho thấy bias hệ thống; case PNAS cho thấy AI không có rào chắn sư phạm có thể làm giảm kết quả học thật. |
| Mobility / autonomous driving | Injury, fatality, public safety risk, trust loss, regulatory suspension và recall trên quy mô đội xe. | Perception / prediction failure, escalation failure, unsafe post-collision behavior, over-reliance, misuse. | Model, Safety, UX, Operations / Governance. | Critical | Severity cao nhất vì lỗi có thể gây chấn thương hoặc tử vong trong vài giây. Scale có thể mở rộng khi lỗi phần mềm nằm trong đội xe hoặc hàng triệu xe hỗ trợ lái. |
| HR / tuyển dụng | Không có dữ liệu case từ nhóm hiện tại. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không chấm | Ngành này nằm trong danh sách lab nhưng không có thành viên nào trong 3 file đầu vào chọn phân tích. |
| Y tế / symptom checker / health assistant | Không có dữ liệu case từ nhóm hiện tại. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không chấm | Ngành này nằm trong danh sách lab nhưng không có thành viên nào trong 3 file đầu vào chọn phân tích. |
| Content creator | Không có dữ liệu case từ nhóm hiện tại. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không đánh giá trong phạm vi báo cáo nhóm này. | Không chấm | Ngành này nằm trong danh sách lab nhưng không có thành viên nào trong 3 file đầu vào chọn phân tích. |

## 5. Tổng Hợp Pattern Rủi Ro Giữa Các Ngành

Ba ngành có bối cảnh khác nhau nhưng cùng cho thấy một điểm chung: rủi ro AI không chỉ nằm ở mô hình, mà nằm ở cả hệ thống triển khai, cơ chế giám sát và trách nhiệm con người.

Trong `Media / News / Social / Political assistant`, harm thường lan truyền qua thông tin sai, thiếu nguồn, trích dẫn sai hoặc vi phạm bản quyền. `Frequency` cao vì người dùng có thể truy vấn tin tức liên tục, và nội dung sai có thể lan rộng nhanh trong môi trường số.

Trong `Giáo dục / AI Tutor`, harm thường xuất hiện qua quyết định thể chế như điểm số, tuyển sinh, kỷ luật học thuật hoặc thiết kế học tập. Đây là ngành có rủi ro dữ liệu nhạy cảm và bất công hệ thống rất rõ, vì người học thường là nhóm dễ bị tổn thương và khó phản kháng.

Trong `Mobility / autonomous driving`, harm có thể xảy ra trực tiếp trong môi trường vật lý. Lỗi nhận diện, lỗi dự đoán, hành vi sau va chạm hoặc chuyển giao trách nhiệm yếu có thể dẫn đến chấn thương hoặc tử vong.

### 5.1. So Sánh Theo 4 Yếu Tố Chấm Rủi Ro

Nếu đặt ba ngành cạnh nhau theo bốn yếu tố của lab, có thể thấy mỗi ngành “nguy hiểm” theo một cách khác nhau. Mobility đứng đầu về `Severity` vì harm có thể là tử vong. Giáo dục nổi bật về `Scale` và hậu quả khó đảo ngược vì quyết định thuật toán có thể ảnh hưởng đến cả cohort học sinh, kỳ tuyển sinh và danh dự học thuật. Media/News nổi bật về `Frequency` vì hệ thống có thể tạo hoặc tổng hợp nội dung liên tục, trong khi lỗi thông tin có thể được lan truyền nhiều lần qua nền tảng số.

| Ngành | Severity | Scale | Probability | Frequency | Nhận định chi tiết |
|---|---|---|---|---|---|
| Media / News / Social / Political assistant | High | High | Medium đến High | High | Severity thường thấp hơn Mobility vì không trực tiếp điều khiển thế giới vật lý, nhưng trong các chủ đề chính trị, y tế, tài chính hoặc khủng hoảng xã hội, thông tin sai có thể gây hậu quả nghiêm trọng. Frequency cao vì tin tức được truy vấn và tái phân phối liên tục. |
| Giáo dục / AI Tutor | High đến Critical | High đến Critical | Medium đến High | Medium | Severity cao vì ảnh hưởng đến điểm số, tuyển sinh, học bổng, kỷ luật và danh dự học thuật. Scale có thể rất lớn khi hệ thống được áp dụng cấp trường, cấp bang hoặc cấp quốc gia như case Ofqual. |
| Mobility / autonomous driving | Critical | Medium đến High | Low đến Medium | Low đến Medium | Probability và Frequency của từng tình huống nguy hiểm có thể thấp hơn tin tức, nhưng Severity cao nhất vì lỗi xảy ra trong vài giây có thể gây chấn thương hoặc tử vong. Khi lỗi nằm trong phần mềm đội xe, Scale có thể tăng mạnh. |

### 5.2. So Sánh Theo Nhu Cầu Kiểm Soát Trước Khi Triển Khai

Ba ngành cũng khác nhau ở mức kiểm soát cần có trước khi đưa sản phẩm ra sử dụng. Media/News cần quy trình biên tập, dẫn nguồn và hạn chế trả lời ở các chủ đề nhạy cảm. Giáo dục cần cơ chế giáo viên quyết định cuối, quy trình khiếu nại, kiểm tra bias và thiết kế sư phạm không cho đáp án trực tiếp một cách thiếu kiểm soát. Mobility cần tiêu chuẩn an toàn nghiêm ngặt nhất: giới hạn phạm vi vận hành, kiểm thử tình huống hiếm, cơ chế dừng an toàn, báo cáo sự cố và can thiệp con người hoặc từ xa khi hệ thống gặp tình huống ngoài thiết kế.

| Ngành | Human-in-the-loop cần ở đâu? | Bar “được ship” nên tập trung vào gì? |
|---|---|---|
| Media / News / Social / Political assistant | Biên tập viên, kiểm chứng nguồn, kiểm tra trích dẫn và rà soát các câu trả lời thuộc chủ đề chính trị, y tế, tài chính. | Độ chính xác nguồn, khả năng từ chối khi thiếu bằng chứng, ghi rõ nguồn, tránh tóm tắt thay thế hoàn toàn bài báo gốc. |
| Giáo dục / AI Tutor | Giáo viên, hội đồng học thuật, quy trình phúc khảo, người giám sát dữ liệu học sinh và thiết kế rào chắn sư phạm. | Công bằng giữa nhóm học sinh, bảo vệ dữ liệu nhạy cảm, không dùng cảnh báo AI làm bằng chứng kỷ luật duy nhất, đo học thật thay vì chỉ đo kết quả khi có AI. |
| Mobility / autonomous driving | Safety operator, remote assistance, cơ chế tiếp quản, quy trình sau va chạm và cơ quan quản lý nhận báo cáo sự cố. | An toàn vật lý, phạm vi vận hành rõ ràng, dừng an toàn, kiểm thử edge case và chứng minh hệ thống giảm harm trong tình huống bất thường. |

## 6. Trả Lời Câu Hỏi Thảo Luận Nhóm

| Câu hỏi thảo luận | Nhận định của nhóm |
|---|---|
| Ngành nào có `Severity` tiềm năng cao nhất? | `Mobility / autonomous driving`, vì lỗi có thể gây chấn thương hoặc tử vong trong thời gian rất ngắn. |
| Ngành nào có `Scale` tiềm năng lớn nhất? | `Giáo dục / AI Tutor` và `Mobility` đều rất lớn. Giáo dục nổi bật ở tác động thể chế với hàng triệu điểm số; Mobility nổi bật ở quy mô sản phẩm với recall hơn 2 triệu xe. |
| Ngành nào có `Probability` hoặc `Frequency` cao nhất? | `Media / News / Social / Political assistant`, vì truy vấn tin tức và tạo nội dung có thể diễn ra liên tục, còn lỗi thông tin có thể lặp lại thường xuyên. |
| Ngành nào xử lý dữ liệu nhạy cảm rõ nhất? | `Giáo dục / AI Tutor`, vì dữ liệu học tập, điểm số, hồ sơ kỷ luật, bài luận, dữ liệu sinh trắc học trong giám sát thi cử và thông tin trẻ vị thành niên đều rất nhạy cảm. |
| Ngành nào cần `human-in-the-loop` rõ nhất? | Cả ba ngành đều cần. Mobility cần can thiệp an toàn tức thời; Giáo dục cần con người quyết định cuối trong chấm điểm/kỷ luật; Media cần biên tập viên xác minh nguồn và nội dung. |
| Ngành nào cần bar “được ship” cao nhất? | `Mobility / autonomous driving` cần bar cao nhất vì lỗi có thể gây harm vật lý trực tiếp. `Giáo dục / AI Tutor` đứng rất gần vì lỗi có thể tạo bất công hệ thống và ảnh hưởng tương lai người học. |

## 7. Kết Luận Nhóm

Qua so sánh ba ngành, nhóm nhận thấy không thể đánh giá rủi ro AI chỉ bằng độ chính xác kỹ thuật. Một hệ thống có thể đạt kết quả tốt trong bài test nhưng vẫn nguy hiểm nếu được triển khai trong bối cảnh có quyết định hệ trọng, dữ liệu nhạy cảm, khả năng lan truyền lớn hoặc harm khó đảo ngược.

Trong ba ngành đã phân tích, `Mobility / autonomous driving` có mức nguy hiểm vật lý cao nhất, `Giáo dục / AI Tutor` có mức rủi ro thể chế và dữ liệu nhạy cảm nổi bật nhất, còn `Media / News / Social / Political assistant` có tần suất lặp lại và tốc độ lan truyền thông tin sai cao nhất. Điểm chung của cả ba là các hệ thống AI cần rào chắn rõ ràng, con người kiểm duyệt có quyền thực sự, minh bạch nguồn và dữ liệu sự cố, cùng tiêu chuẩn triển khai cao hơn khi hệ thống chạm đến quyết định hệ trọng.

## 8. Tài Liệu Đầu Vào

- `VoTanTrung-report.md` - Báo cáo ngành Trợ lý Tin tức AI / Media / News của Võ Tấn Trung.
- `NguyenHoangThanhTung-report.md` - Báo cáo ngành Giáo dục / AI Tutor của Nguyễn Hoàng Thanh Tùng.
- `NguyenMinhDuc-report.md` - Báo cáo ngành Mobility / autonomous driving của Nguyễn Minh Đức.
