Dựa trên kết quả benchmark, mô hình hoàn thành huấn luyện trong thời gian rất ngắn (1.38 giây) và đạt chất lượng dự đoán xuất sắc với chỉ số AUC-ROC là 0.9367. Tốc độ suy luận (inference) phản hồi nhanh, chỉ mất 0.44 ms cho một dòng dữ liệu và 0.56 ms để xử lý 1000 dòng.

Về mặt hạ tầng, hệ thống phải triển khai bằng kiến trúc CPU Fallback (sử dụng máy r5.xlarge) thay vì GPU (g4dn.xlarge) như thiết kế chuẩn. Nguyên nhân trực tiếp là do tài khoản AWS đang bị giới hạn Quota mặc định (mức 0 vCPU cho các dòng máy G-instances).
