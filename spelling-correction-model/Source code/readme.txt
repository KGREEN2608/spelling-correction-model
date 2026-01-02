Fine-tune mô hình VietAI/vit5-base cho bài toán sửa lỗi văn bản hành chính .
----------------------------------------------------

Mã nguồn được chạy trên Google Colaboratory với GPU là A100.

Hướng dẫn chạy mã nguồn:

Bước 1: Upload dữ liệu cần thiết gồm train_data.txt, val_data.txt và test.txt.

Bước 2: Sử dụng tệp train_data.txt và val_data.txt để fine-tune mô hình:
trainer = VietnameseTextCorrectionTrainer(
    model_name="VietAI/vit5-base",
    output_dir=f"./results_vit5_base_V1"
)

train_dataset = trainer.prepare_data("/content/train_data.txt")

val_dataset = trainer.prepare_data("/content/val_data.txt")


trainer.train(train_dataset,val_dataset,num_epochs=3, batch_size=16, learning_rate=3e-5)

Bước 3: Sau khi hoàn thành quá trình fine-tune thì đẩy mô hình đã lưu lên huggingface TranKhang/DACNTT_viT5_base_V1 để có thể sử dụng về sau.

Bước 4: Dùng mô hình đã lưu trên huggingface để đánh giá tệp test_data.txt bằng hàm evaluate_model_with_logprob. Lưu kết quả vào tệp evaluation_results.json gồm Corrupted text,Prediction,Original text .

Bước 5: Chạy hàm load_and_evaluate_json_file để đọc tệp evaluation_results.json và evaluate_json_file cho việc đánh giá mô hình.