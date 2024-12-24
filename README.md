# 2025-message
// api/messages.js
export default function handler(req, res) {
    if (req.method === 'POST') {
        // Xử lý logic gửi tin nhắn ở đây
        const { name, message } = req.body;
        // Lưu tin nhắn (có thể cần cơ sở dữ liệu hoặc lưu trữ cục bộ)
        
        // Phản hồi với thành công
        return res.status(200).json({ success: true });
    } else {
        // Xử lý bất kỳ phương thức HTTP nào khác
        res.setHeader('Allow', ['POST']);
        return res.status(405).end(`Method ${req.method} Not Allowed`);
    }
}
