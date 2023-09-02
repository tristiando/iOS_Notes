# Update a specific old commit

Dùng `git rebase` để chỉnh sửa một commit cũ. Ví dụ với danh sách commit sau khi `git log` như sau:

<figure><img src="../.gitbook/assets/Screen Shot 2023-09-02 at 21.14.30.png" alt=""><figcaption><p>Danh sách commit sau khi <code>git log</code>. Commit <code>8d80</code> là commit mới nhất.</p></figcaption></figure>

commit `8d80` `Remove unused FeedViewModel..`

commit `fa10` `Move memory management..` <-- là commit cần được chỉnh sửa

commit `ff69` `Add FeedPresenter..`

Ta dùng lệnh `git rebase -i ff69..` để bắt đầu:

<figure><img src="../.gitbook/assets/Screen Shot 2023-09-02 at 21.20.41 copy.jpg" alt=""><figcaption></figcaption></figure>

