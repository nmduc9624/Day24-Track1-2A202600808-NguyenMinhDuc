# Báo Cáo Cá Nhân Day 24 Track 1

Tên repo dự kiến: `Day24-Track1-2A202600808-NguyenMinhDuc`

Mã học viên: `2A202600808`

Họ và tên: `Nguyễn Minh Đức`

Ngành đã chọn: `Mobility / autonomous driving`

## 1. Tóm Tắt Báo Cáo

Báo cáo này phân tích rủi ro của AI trong ngành `Mobility / autonomous driving`, tập trung vào các hệ thống xe tự lái, robotaxi và hệ thống hỗ trợ lái nâng cao. Đây là một trong những lĩnh vực AI có mức độ rủi ro cao nhất vì hệ thống không chỉ xử lý thông tin, mà còn tác động trực tiếp đến chuyển động của phương tiện trong môi trường giao thông thật. Khi hệ thống nhận diện sai, dự đoán sai, chuyển giao trách nhiệm không rõ ràng hoặc khiến con người quá tin vào khả năng tự động hóa, hậu quả có thể là va chạm, chấn thương, tử vong, đình chỉ vận hành hoặc mất niềm tin công chúng.

Ba case được chọn trong báo cáo gồm: vụ xe tự lái Uber gây chết người tại Tempe năm 2018, vụ robotaxi Cruise kéo lê người đi bộ tại San Francisco năm 2023, và vụ Tesla Autopilot / Autosteer recall hơn 2 triệu xe tại Mỹ năm 2023. Ba case này đại diện cho ba nhóm rủi ro quan trọng của ngành: lỗi nhận diện và phản ứng trong tình huống nguy hiểm, lỗi hành vi an toàn sau va chạm ở robotaxi không người lái, và rủi ro `over-reliance` khi người lái hiểu sai năng lực của hệ thống hỗ trợ lái cấp độ 2.

Kết luận chính của báo cáo là `risk profile` tổng thể của ngành `Mobility / autonomous driving` nên được xếp ở mức `Critical`. Lý do là `Severity` tiềm năng rất cao, thời gian can thiệp ngắn, môi trường vận hành phức tạp, và một lỗi thiết kế có thể ảnh hưởng đến cả đội xe hoặc hàng triệu phương tiện nếu được triển khai rộng.

## 2. Phương Pháp Chọn Và Phân Tích Case

Các case trong báo cáo được chọn theo ba tiêu chí. Thứ nhất, case phải là sự kiện có thật, có nguồn đáng tin cậy và có thể kiểm chứng. Thứ hai, case phải có ít nhất một số liệu cụ thể để phục vụ phân tích, ví dụ số người bị ảnh hưởng, số xe bị recall, thời điểm xảy ra sự cố hoặc thông tin kỹ thuật quan trọng. Thứ ba, case phải đủ dữ kiện để phân tích bằng `Harm Map Worksheet`, bao gồm bên liên quan bị ảnh hưởng, `failure mode`, `layer` bắt đầu lỗi, loại harm, `Severity`, `Scale`, `Probability` và `Frequency`.

Nguồn được ưu tiên là nguồn chính thức từ cơ quan điều tra hoặc cơ quan quản lý, chẳng hạn NTSB, California DMV và NHTSA. Các nguồn báo chí chất lượng cao như Associated Press và Wired được dùng để đối chiếu, bổ sung bối cảnh và giúp diễn giải sự kiện rõ hơn. Báo cáo không sử dụng công cụ trò chuyện AI làm nguồn cho sự kiện.

## 3. Industry Risk Snapshot

Ngành `Mobility / autonomous driving` có đặc điểm khác với nhiều ngành AI khác vì sai sót của hệ thống có thể chuyển thành rủi ro vật lý ngay lập tức. Trong môi trường giao thông, xe phải xử lý đồng thời người đi bộ, xe máy, ô tô, xe đạp, biển báo, thời tiết, vật cản, công trình, hành vi bất ngờ của con người và các tình huống ngoài phạm vi thiết kế vận hành. Chỉ một quyết định sai trong vài giây cũng có thể dẫn đến hậu quả nghiêm trọng.

| Câu hỏi | Mức độ | Phân tích |
|---|---|---|
| Nếu AI sai, có thể gây hại thể chất không? | Critical | Có. Hệ thống có thể điều khiển hoặc ảnh hưởng đến phanh, đánh lái, tăng tốc, giảm tốc và dừng khẩn cấp. Nếu nhận diện sai người đi bộ, dự đoán sai hướng di chuyển của phương tiện khác hoặc không phản ứng kịp, hậu quả có thể là va chạm, chấn thương hoặc tử vong. |
| AI có ảnh hưởng đến quyết định hệ trọng không? | Critical | Có. Trong xe tự lái hoặc hệ thống hỗ trợ lái, AI tham gia vào các quyết định trực tiếp liên quan đến an toàn giao thông. Các quyết định này thường phải được đưa ra trong thời gian rất ngắn, nên lỗi nhỏ trong nhận diện hoặc chuyển giao quyền kiểm soát có thể gây hậu quả lớn. |
| Hệ thống có động tới dữ liệu nhạy cảm không? | High | Có. Hệ thống có thể xử lý hình ảnh camera, vị trí, hành trình, hành vi lái xe, video đường phố, dữ liệu cảm biến và thông tin người dùng. Nếu dữ liệu này bị lộ, lưu trữ sai cách hoặc dùng sai mục đích, có thể tạo rủi ro về quyền riêng tư và giám sát. |
| Nếu sai, hậu quả có khó đảo ngược không? | Critical | Có. Chấn thương, tử vong và thiệt hại vật chất ngoài đời thực không thể khôi phục hoàn toàn. Bên cạnh đó, sau một sự cố nghiêm trọng, doanh nghiệp có thể bị đình chỉ vận hành, recall sản phẩm, mất niềm tin và chịu rủi ro pháp lý. |
| Nếu triển khai rộng, `blast radius` có lớn không? | High | Có. Một lỗi phần mềm có thể ảnh hưởng đến cả đội xe robotaxi hoặc hàng triệu xe hỗ trợ lái nếu cùng dùng một phiên bản hệ thống. Case Tesla cho thấy recall có thể mở rộng đến hơn 2 triệu phương tiện tại Mỹ. |
| Có cần `human review` hoặc `escalation` không? | Critical | Có. Ngành này cần cơ chế con người giám sát, tiếp quản, hỗ trợ từ xa, xử lý tình huống ngoài phạm vi vận hành và báo cáo sự cố. Tuy nhiên, nếu thiết kế chuyển giao trách nhiệm không rõ ràng, con người có thể không kịp can thiệp. |
| `Risk profile` tổng thể của ngành | Critical | Mức rủi ro tổng thể là `Critical` vì harm tiềm năng có thể là chấn thương hoặc tử vong, trong khi môi trường vận hành lại phức tạp, khó dự đoán và có nhiều tác nhân cùng tương tác. |

## 4. Case 01 - Vụ Xe Tự Lái Uber Gây Chết Người Tại Tempe Năm 2018

### 4.1. Tổng Quan Case

Case Uber tại Tempe là một trong những sự kiện quan trọng nhất trong lịch sử thử nghiệm xe tự lái trên đường công cộng. Ngày 18/03/2018, một xe thử nghiệm của Uber Advanced Technologies Group đang chạy ở chế độ tự động tại Tempe, Arizona thì đâm vào Elaine Herzberg, một người đi bộ đang dắt xe đạp qua đường. Nạn nhân tử vong sau vụ va chạm. Đây được xem là một trong những vụ tử vong đầu tiên liên quan đến xe thử nghiệm tự lái trên đường công cộng.

Điểm đáng chú ý của case này là xe không vận hành trong môi trường đóng, mà đang được thử nghiệm trên đường thật, có người vận hành an toàn ngồi sau vô lăng. Theo báo cáo của NTSB, hệ thống đã phát hiện đối tượng trước va chạm nhưng phân loại và dự đoán không ổn định. Đồng thời, cơ chế phanh khẩn cấp và cơ chế cảnh báo cho người vận hành an toàn không đủ hiệu quả để tránh tai nạn. Case này vì vậy không chỉ là lỗi của một mô hình nhận diện, mà là thất bại tổng hợp của `Model`, `Safety`, `UX` và quản trị an toàn.

### 4.2. Brief Case

| Mục | Nội dung |
|---|---|
| Tên case | Vụ xe tự lái Uber gây chết người tại Tempe |
| Ngành | `Mobility / autonomous driving` |
| Tổ chức / sản phẩm | Uber Advanced Technologies Group; xe Volvo XC90 được chỉnh sửa để thử nghiệm hệ thống tự lái |
| `Use case AI` | Xe thử nghiệm tự lái chạy trên đường công cộng, có người vận hành an toàn ngồi sau vô lăng để giám sát và can thiệp khi cần. |
| Thời điểm | Ngày 18/03/2018, tại Tempe, Arizona, Mỹ |
| Case xảy ra chuyện gì? | Xe thử nghiệm của Uber đang chạy ở chế độ tự động thì đâm vào Elaine Herzberg, người đang dắt xe đạp qua đường. Hệ thống không phanh khẩn cấp kịp thời và người vận hành an toàn cũng không can thiệp đủ sớm. Vụ việc dẫn đến một ca tử vong và khiến hoạt động thử nghiệm của Uber bị xem xét nghiêm ngặt. |
| Bên liên quan bị ảnh hưởng | Người đi bộ, người vận hành an toàn, Uber ATG, cơ quan quản lý giao thông, người dân địa phương và ngành xe tự lái. |
| Số liệu chính | Báo cáo NTSB nêu rằng hệ thống bắt đầu phát hiện người đi bộ khoảng 5,6 giây trước va chạm; xe đã chạy ở chế độ tự động khoảng 19 phút trước khi xảy ra tai nạn; vụ việc gây 1 ca tử vong. |
| Nguồn 1 | National Transportation Safety Board, báo cáo HAR-19/03: https://www.ntsb.gov/investigations/AccidentReports/Reports/HAR1903.pdf |
| Nguồn 2 | Wired, bài viết đối chiếu về báo cáo NTSB: https://www.wired.com/story/uber-self-driving-crash-arizona-ntsb-report |
| Độ tin cậy của nguồn | Nguồn NTSB là nguồn chính thức từ cơ quan điều tra tai nạn giao thông, có độ tin cậy cao. Wired được dùng để đối chiếu và diễn giải bối cảnh. |

### 4.3. Harm Map Worksheet

| Khoảnh khắc rủi ro cao | Bên liên quan bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Phân tích |
|---|---|---|---|---|---|---|---|---|---|---|
| Xe tự lái gặp người đi bộ băng qua đường vào ban đêm, ngoài vạch qua đường | Người đi bộ | Lỗi nhận diện và phân loại đối tượng | Model | Hệ thống không duy trì được nhận diện ổn định về người đi bộ, dẫn đến không phản ứng kịp | Injury | Critical | Low | Medium | Low | Harm có thể là tử vong, nên `Severity` là `Critical`. `Scale` thấp vì đây là một xe thử nghiệm cụ thể, nhưng `Probability` ở mức trung bình vì đường phố thật thường có người đi bộ và tình huống bất thường. |
| Hệ thống không phanh khẩn cấp đúng lúc | Người đi bộ, người vận hành an toàn | Escalation failure | Safety | Xe không tự phanh kịp và cũng không tạo điều kiện đủ tốt để con người can thiệp | Injury | Critical | Low | Medium | Low | Đây là lỗi ở tầng an toàn. Nếu hệ thống đã nhận ra tình huống nguy hiểm nhưng không phanh hoặc không cảnh báo đủ mạnh, cơ chế giảm thiểu harm không còn hiệu quả. |
| Người vận hành an toàn phải giám sát hệ thống trong môi trường lái đơn điệu | Người vận hành an toàn, người đi đường | Over-reliance và lỗi giám sát của con người | UX | Người vận hành mất tập trung, không phản ứng đủ nhanh trong thời điểm nguy hiểm | Injury | Critical | Low | Medium | Medium | Thiết kế yêu cầu con người giám sát thụ động trong thời gian dài là rủi ro lớn. Con người khó duy trì sự chú ý tuyệt đối khi hệ thống phần lớn thời gian tự vận hành. |
| Chương trình thử nghiệm chưa có hàng rào an toàn đủ mạnh trước khi đưa xe ra đường công cộng | Công chúng, Uber, cơ quan quản lý | Lỗi quản trị an toàn | Safety | Rủi ro thử nghiệm vượt quá khả năng kiểm soát, gây mất niềm tin và hệ quả pháp lý | Public safety / trust loss | High | Medium | Medium | Low | Case này cho thấy safety không chỉ là vấn đề kỹ thuật. Quy trình thử nghiệm, văn hóa an toàn, đào tạo người vận hành và tiêu chuẩn triển khai đều ảnh hưởng trực tiếp đến rủi ro. |

### 4.4. Nhận Định Case

Case Uber cho thấy rủi ro nghiêm trọng nhất của xe tự lái không nằm ở một điểm lỗi đơn lẻ, mà nằm ở chuỗi lỗi liên hoàn. Hệ thống nhận diện chưa đủ chắc chắn, cơ chế phanh và cảnh báo không đủ mạnh, người vận hành an toàn không được hỗ trợ đúng cách, và quy trình thử nghiệm chưa tạo đủ lớp bảo vệ. Trong một ngành safety-critical, các lớp bảo vệ phải được thiết kế để khi một lớp thất bại, lớp khác vẫn có thể giảm harm. Ở case này, nhiều lớp cùng thất bại trong cùng một khoảnh khắc.

## 5. Case 02 - Robotaxi Cruise Kéo Lê Người Đi Bộ Tại San Francisco Năm 2023

### 5.1. Tổng Quan Case

Cruise là dịch vụ robotaxi không người lái do General Motors hậu thuẫn, từng được xem là một trong những đơn vị đi đầu trong triển khai xe tự lái thương mại tại San Francisco. Case tháng 10/2023 trở thành sự kiện lớn vì nó không chỉ liên quan đến một va chạm, mà còn liên quan đến cách xe xử lý sau va chạm và cách doanh nghiệp cung cấp thông tin cho cơ quan quản lý.

Ngày 02/10/2023, một người đi bộ bị một xe do con người lái tông trước, sau đó rơi vào đường đi của xe Cruise. Xe Cruise tiếp tục liên quan đến va chạm và sau đó thực hiện thao tác tấp vào lề, khiến người đi bộ bị kéo lê. Sau sự cố, California DMV đình chỉ giấy phép vận hành không người lái của Cruise vào ngày 24/10/2023. Associated Press sau đó đưa tin Cruise recall 950 xe để cập nhật phần mềm. Case này đặc biệt quan trọng vì nó cho thấy hệ thống tự lái cần được đánh giá không chỉ ở khả năng tránh va chạm, mà còn ở hành vi sau va chạm, minh bạch dữ liệu và trách nhiệm với cơ quan quản lý.

### 5.2. Brief Case

| Mục | Nội dung |
|---|---|
| Tên case | Robotaxi Cruise kéo lê người đi bộ và bị đình chỉ giấy phép |
| Ngành | `Mobility / autonomous driving` |
| Tổ chức / sản phẩm | Cruise LLC, dịch vụ robotaxi không người lái do General Motors hậu thuẫn |
| `Use case AI` | Robotaxi không có tài xế an toàn trong xe, vận hành trên đường phố công cộng tại San Francisco. |
| Thời điểm | Tai nạn ngày 02/10/2023; California DMV đình chỉ giấy phép ngày 24/10/2023; Cruise recall ngày 08/11/2023 |
| Case xảy ra chuyện gì? | Một người đi bộ bị xe khác tông trước rồi rơi vào đường đi của xe Cruise. Xe Cruise liên quan đến va chạm và sau đó thực hiện thao tác tấp vào lề, khiến người đi bộ bị kéo lê. California DMV đình chỉ giấy phép của Cruise vì cho rằng phương tiện tạo rủi ro không hợp lý đối với an toàn công cộng và doanh nghiệp đã trình bày thiếu hoặc sai lệch thông tin liên quan đến sự cố. |
| Bên liên quan bị ảnh hưởng | Người đi bộ, người dân San Francisco, hành khách robotaxi, Cruise, General Motors, California DMV, chính quyền thành phố và công chúng. |
| Số liệu chính | Cruise recall 950 xe không người lái để cập nhật phần mềm sau vụ việc; California DMV đình chỉ giấy phép vận hành không người lái của Cruise vào ngày 24/10/2023. |
| Nguồn 1 | California DMV, thông báo đình chỉ Cruise LLC: https://www.dmv.ca.gov/portal/news-and-media/dmv-statement-on-cruise-llc-suspension/ |
| Nguồn 2 | Associated Press, bài viết về việc Cruise recall 950 xe: https://apnews.com/article/bf08c0c6e7914649750b4dde598af5fc |
| Độ tin cậy của nguồn | California DMV là nguồn chính thức của cơ quan quản lý. Associated Press là nguồn báo chí chất lượng cao, cung cấp thêm số liệu recall và bối cảnh sự kiện. |

### 5.3. Harm Map Worksheet

| Khoảnh khắc rủi ro cao | Bên liên quan bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Phân tích |
|---|---|---|---|---|---|---|---|---|---|---|
| Robotaxi gặp tình huống sau va chạm phức tạp: người đi bộ bị xe khác tông rồi rơi vào đường xe Cruise | Người đi bộ | Lỗi nhận diện và theo dõi trạng thái đối tượng | Model | Hệ thống không hiểu đủ chính xác vị trí, trạng thái và mức độ nguy hiểm của người đi bộ sau va chạm | Injury | Critical | Medium | Medium | Low | Tình huống này không xảy ra thường xuyên, nhưng trong đô thị đông đúc, các tình huống bất thường vẫn có thể xuất hiện. Nếu hệ thống không xử lý được ngoại lệ nghiêm trọng, hậu quả có thể rất lớn. |
| Xe thực hiện thao tác tấp vào lề sau khi đã liên quan đến va chạm | Người đi bộ | Hành vi sau va chạm gây hại | Safety | Người đi bộ bị kéo lê, làm harm có thể nặng hơn so với va chạm ban đầu | Injury | Critical | Medium | Low | Low | Sau va chạm, hành vi an toàn tối thiểu nên ưu tiên dừng lại, cảnh báo và chờ hỗ trợ. Việc tiếp tục di chuyển trong trạng thái chưa hiểu rõ môi trường có thể làm nặng thêm chấn thương. |
| Doanh nghiệp cung cấp thông tin chưa đầy đủ cho cơ quan quản lý | Cơ quan quản lý, công chúng, Cruise | Lỗi minh bạch và quản trị | Safety | Cơ quan quản lý và công chúng không có đủ dữ kiện để đánh giá đúng rủi ro | Public trust / safety governance | High | High | Medium | Medium | Với xe tự lái, dữ liệu sự cố là một phần của safety case. Thiếu minh bạch không chỉ gây rủi ro uy tín mà còn làm giảm khả năng giám sát của cơ quan quản lý. |
| Đội xe robotaxi vận hành trên đường công cộng khi hành vi sau va chạm chưa đủ an toàn | Người đi đường, hành khách, thành phố | Triển khai quá sớm | Safety | Lỗi logic có thể lặp lại ở nhiều xe trong cùng đội xe | Injury / trust loss | Critical | Medium | Medium | Medium | Recall 950 xe cho thấy vấn đề có thể là lỗi cấp phần mềm hoặc cấp đội xe. Khi một lỗi tồn tại trong hệ thống chung, `Scale` không còn giới hạn ở một phương tiện. |

### 5.4. Nhận Định Case

Case Cruise nhấn mạnh rằng xe tự lái phải được thiết kế cho cả tình huống trước, trong và sau va chạm. Một hệ thống có thể chạy tốt trong phần lớn chuyến đi nhưng vẫn không đủ an toàn nếu thất bại trong tình huống hiếm có mức nguy hiểm cao. Ngoài ra, case này cho thấy `Safety` không chỉ là năng lực kỹ thuật của xe mà còn bao gồm minh bạch, báo cáo sự cố, hợp tác với cơ quan quản lý và khả năng chứng minh rằng hệ thống đủ an toàn để vận hành trên đường công cộng.

## 6. Case 03 - Tesla Autopilot / Autosteer Recall Năm 2023

### 6.1. Tổng Quan Case

Tesla Autopilot / Autosteer không phải là xe tự lái hoàn toàn. Đây là hệ thống hỗ trợ lái cấp độ 2, nghĩa là xe có thể hỗ trợ giữ làn, điều chỉnh tốc độ và đánh lái trong một số điều kiện, nhưng người lái vẫn phải chú ý và chịu trách nhiệm liên tục. Chính điểm này tạo ra một rủi ro quan trọng: người dùng có thể hiểu sai năng lực của hệ thống, tin rằng xe tự lái nhiều hơn thực tế và giảm mức độ giám sát.

Tháng 12/2023, Tesla recall hơn 2 triệu xe tại Mỹ để cập nhật phần mềm liên quan đến cơ chế giám sát người lái khi dùng Autopilot / Autosteer. Associated Press và Wired đều đưa tin recall này diễn ra sau quá trình NHTSA xem xét rủi ro người lái dùng sai cách hoặc không duy trì sự chú ý khi hệ thống hỗ trợ lái đang hoạt động. Case này khác với Uber và Cruise ở chỗ nó không chỉ liên quan đến một xe hay một sự cố cụ thể, mà liên quan đến rủi ro cấp đội xe trên quy mô rất lớn.

### 6.2. Brief Case

| Mục | Nội dung |
|---|---|
| Tên case | Tesla Autopilot / Autosteer recall do rủi ro người lái dùng sai cách |
| Ngành | `Mobility / autonomous driving` |
| Tổ chức / sản phẩm | Tesla Autopilot / Autosteer trên Model S, Model X, Model 3 và Model Y |
| `Use case AI` | Hệ thống hỗ trợ lái nâng cao, hỗ trợ giữ làn, điều chỉnh tốc độ và đánh lái trong một số điều kiện nhất định. Hệ thống vẫn yêu cầu người lái giám sát liên tục. |
| Thời điểm | Recall công bố ngày 12-13/12/2023; NHTSA tiếp tục theo dõi hiệu quả recall trong năm 2024 |
| Case xảy ra chuyện gì? | Tesla recall hơn 2 triệu xe tại Mỹ để cập nhật phần mềm, sau khi cơ quan quản lý xem xét việc Autopilot / Autosteer có thể chưa đủ ràng buộc và cảnh báo để ngăn người lái dùng sai cách hoặc mất tập trung. Case này thể hiện rủi ro `over-reliance`, trong đó người lái có thể đánh giá quá cao năng lực tự động hóa và không sẵn sàng tiếp quản khi cần. |
| Bên liên quan bị ảnh hưởng | Người lái Tesla, hành khách, người đi đường, Tesla, NHTSA và công chúng. |
| Số liệu chính | Recall liên quan đến hơn 2 triệu xe tại Mỹ; mã recall thường được nhắc tới là NHTSA Campaign `23V838000`. |
| Nguồn 1 | Associated Press, bài viết về Tesla recall hơn 2 triệu xe: https://apnews.com/article/8060508627a34e6af889feca46eb3002 |
| Nguồn 2 | Wired, bài viết đối chiếu về lỗi Autopilot: https://www.wired.com/story/tesla-us-recall-autopilot-fault |
| Độ tin cậy của nguồn | Associated Press và Wired là các nguồn báo chí chất lượng cao, dựa trên thông tin từ NHTSA và Tesla. Số liệu recall hơn 2 triệu xe là số liệu được nhiều nguồn uy tín ghi nhận. |

### 6.3. Harm Map Worksheet

| Khoảnh khắc rủi ro cao | Bên liên quan bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Phân tích |
|---|---|---|---|---|---|---|---|---|---|---|
| Người lái bật Autopilot / Autosteer trong điều kiện không phù hợp hoặc không giám sát liên tục | Người lái, hành khách, người đi đường | Over-reliance / misuse | UX | Người lái tin hệ thống tự động hơn năng lực thực tế, dẫn đến phản ứng chậm khi cần tiếp quản | Injury | Critical | High | Medium | Medium | Hệ thống cấp độ 2 vẫn cần con người chịu trách nhiệm. Nếu giao diện, tên gọi, cảnh báo hoặc trải nghiệm sử dụng khiến người lái chủ quan, harm có thể xảy ra trên quy mô lớn. |
| Hệ thống giám sát người lái không đủ mạnh để bảo đảm người lái chú ý | Người lái, người đi đường | Giám sát yếu / Escalation failure | Safety | Hệ thống tiếp tục hoạt động dù người lái không chú ý đủ mức | Injury | High | High | Medium | Medium | Recall hơn 2 triệu xe cho thấy đây là rủi ro cấp đội xe. Dù không phải mọi lần dùng đều nguy hiểm, quy mô triển khai lớn làm tăng tổng rủi ro xã hội. |
| Autosteer gặp tình huống ngoài thiết kế, nhưng người lái không kịp nhận ra | Người lái, hành khách, phương tiện khác | Giới hạn nhận diện/lập kế hoạch cộng với lỗi chuyển giao cho con người | Model / UX | Va chạm xảy ra vì hệ thống không xử lý được tình huống và con người không tiếp quản kịp | Injury | Critical | High | Low | Medium | Xác suất mỗi lần lái có thể thấp, nhưng khi hàng triệu xe sử dụng thường xuyên, tần suất sự cố tiềm năng trở nên đáng kể. |
| Biện pháp khắc phục chủ yếu thông qua cập nhật phần mềm từ xa | Người dùng Tesla, cơ quan quản lý, công chúng | Khoảng trống trong bảo đảm an toàn sau recall | Safety | Nếu cập nhật không thay đổi đủ hành vi người dùng, rủi ro `over-reliance` vẫn có thể tồn tại | Public safety / trust loss | High | High | Medium | Medium | Với hệ thống hỗ trợ lái quy mô lớn, khắc phục không chỉ là thêm cảnh báo. Cần theo dõi dữ liệu sau cập nhật để chứng minh người lái thật sự giám sát tốt hơn. |

### 6.4. Nhận Định Case

Case Tesla cho thấy rủi ro lớn của hệ thống hỗ trợ lái không chỉ nằm ở năng lực kỹ thuật, mà còn nằm ở cách con người hiểu và sử dụng hệ thống. Một hệ thống cấp độ 2 có thể bị dùng như hệ thống tự lái nếu người lái tin rằng xe có thể tự xử lý nhiều hơn thực tế. Vì vậy, `UX`, tên gọi tính năng, cảnh báo, giới hạn phạm vi sử dụng và cơ chế giám sát người lái đều là thành phần an toàn. Khi quy mô triển khai lên tới hàng triệu xe, một thiết kế gây hiểu nhầm nhỏ cũng có thể trở thành rủi ro xã hội lớn.

## 7. So Sánh Và Tổng Hợp Pattern Rủi Ro

Ba case có bối cảnh khác nhau nhưng cùng cho thấy một pattern chung: trong `Mobility / autonomous driving`, harm thường xuất hiện khi hệ thống tự động hóa gặp tình huống ngoài kỳ vọng, trong khi các lớp bảo vệ bổ sung không đủ mạnh để ngăn hậu quả. Với Uber, lớp nhận diện và phản ứng không đủ an toàn trong tình huống người đi bộ qua đường. Với Cruise, hành vi sau va chạm và quy trình minh bạch với cơ quan quản lý trở thành điểm yếu. Với Tesla, rủi ro nằm ở việc người lái quá tin vào hệ thống hỗ trợ lái và không duy trì giám sát.

| Case | Harm chính | Failure mode nổi bật | Layer nổi bật | Risk profile |
|---|---|---|---|---|
| Uber Tempe 2018 | Tử vong của người đi bộ, mất niềm tin vào thử nghiệm xe tự lái | Lỗi nhận diện, `escalation failure`, lỗi giám sát của con người | Model, Safety, UX | Critical |
| Cruise San Francisco 2023 | Chấn thương người đi bộ, đình chỉ giấy phép, mất niềm tin công chúng | Hành vi sau va chạm gây hại, lỗi minh bạch, triển khai quá sớm | Model, Safety, Governance | Critical |
| Tesla Autopilot 2023 | Rủi ro va chạm do người lái dùng sai cách hoặc quá tin vào hệ thống | Over-reliance, misuse, giám sát người lái chưa đủ mạnh | UX, Safety | High đến Critical |

Từ ba case, có thể rút ra bốn pattern rủi ro chính. Thứ nhất, lỗi trong nhận diện và dự đoán có thể nhanh chóng chuyển thành harm vật lý. Thứ hai, cơ chế chuyển giao giữa máy và con người thường là điểm yếu vì con người khó phản ứng kịp nếu chỉ được đặt vào vai trò giám sát thụ động. Thứ ba, hành vi sau sự cố cũng quan trọng như hành vi trước sự cố; một xe tự lái phải biết dừng an toàn và giảm harm sau va chạm. Thứ tư, minh bạch với cơ quan quản lý là một phần của an toàn, vì nếu dữ liệu sự cố không được cung cấp đầy đủ, xã hội không thể đánh giá đúng mức rủi ro.

## 8. Kết Luận

Ngành `Mobility / autonomous driving` cần được đánh giá ở mức `Critical` vì AI trong lĩnh vực này tác động trực tiếp đến an toàn thân thể và vận hành trong môi trường khó kiểm soát. Các case Uber, Cruise và Tesla cho thấy rủi ro không chỉ đến từ mô hình AI, mà còn từ toàn bộ hệ thống sản phẩm: thiết kế trải nghiệm, giám sát người dùng, quy trình thử nghiệm, cơ chế dừng an toàn, quản trị sự cố và minh bạch với cơ quan quản lý.

Nếu xây dựng hoặc đánh giá một sản phẩm trong ngành này, các ưu tiên an toàn cần bao gồm: giới hạn rõ phạm vi vận hành, kiểm thử các tình huống hiếm nhưng nguy hiểm, thiết kế cơ chế dừng an toàn sau va chạm, tăng cường giám sát người lái trong hệ thống cấp độ 2, giảm khả năng người dùng hiểu nhầm năng lực tự động hóa, và thiết lập quy trình báo cáo sự cố minh bạch. Trong lĩnh vực này, tiêu chuẩn “đủ tốt để ship” phải cao hơn nhiều so với các ứng dụng AI thông thường, vì một lỗi nhỏ có thể gây hậu quả ngoài đời thực.

## 9. Tài Liệu Tham Khảo

- National Transportation Safety Board. Báo cáo HAR-19/03 về vụ xe thử nghiệm Uber va chạm với người đi bộ: https://www.ntsb.gov/investigations/AccidentReports/Reports/HAR1903.pdf
- Wired. Bài viết đối chiếu về vụ xe tự lái Uber tại Arizona: https://www.wired.com/story/uber-self-driving-crash-arizona-ntsb-report
- California DMV. Thông báo đình chỉ Cruise LLC: https://www.dmv.ca.gov/portal/news-and-media/dmv-statement-on-cruise-llc-suspension/
- Associated Press. Bài viết về việc California đình chỉ hoạt động robotaxi Cruise: https://apnews.com/article/8aa872f6b87bbff59e9c86471e87b0e7
- Associated Press. Bài viết về việc Cruise recall 950 xe sau vụ kéo lê người đi bộ: https://apnews.com/article/bf08c0c6e7914649750b4dde598af5fc
- Associated Press. Bài viết về Tesla recall hơn 2 triệu xe tại Mỹ để sửa cơ chế giám sát người lái khi dùng Autopilot: https://apnews.com/article/8060508627a34e6af889feca46eb3002
- Wired. Bài viết đối chiếu về lỗi Autopilot và recall của Tesla: https://www.wired.com/story/tesla-us-recall-autopilot-fault
