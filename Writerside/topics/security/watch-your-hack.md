# Watch Your Hack

Bài viết được cập nhật lần cuối theo phiên bản: Watch Your Hack V5. Những thay đổi khác nếu có là do tôi thực hiện để làm rõ ý, tránh cho bạn đọc hiểu không đúng vấn đề.

Một phiên bản hoàn thiện của các nội dung trong bài viết chiếm khoảng 20-30% nội dung của khóa huấn luyện của tôi thực hành chi tiết hơn về bảo mật cho tài khoản cá nhân dành cho người nổi tiếng (Celebrity), nhà hoạt động xã hội (social activists), nhà báo (journalists), luật sư (lawyers), giám đốc và những người giữ vị trí quan trọng trong các công ty - VITO (Very Important Top Officer: CEO, CIO, CTO, CFO, CISO, leaders,...) hay đơn giản hơn là những người muốn bảo vệ tài khoản tín dụng ngân hàng của họ.

* Bạn có lo lắng người tình của bạn đã xâm nhập tài khoản Facebook của bạn? Hay bạn lo lắng máy tính của bạn đang bị tống tiền bởi ransomware? Hay bạn lo lắng các hacker đang rút tiền từ tài khoản ngân hàng của bạn?
* Tài liệu này bao gồm các nội dung chính sau: [Hacker là ai](#hacker-l-ai). [Nhập môn](#nh-p-m-n). [Máy tính](#m-y-t-nh). [Điện thoại và máy tính bảng](#i-n-tho-i-v-m-y-t-nh-b-ng). [Mạng xã hội và truyền thông](#m-ng-x-h-i-v-truy-n-th-ng). [Nhắn tin và gọi điện thoại](#nh-n-tin-v-g-i-i-n-tho-i). [Các chủ đề nâng cao](#c-c-ch-n-ng-cao). [Ghi chú và lời kết](#ghi-ch-v-l-i-k-t).

* Tài liệu này giải thích làm thế nào bảo vệ bạn trước các hacker, với ngôn ngữ phổ thông, bình dân nhất. Đã có 6 chuyên gia bảo mật (professional hackers) giúp đỡ tạo bài hướng dẫn này.
* Chú ý là Watch Your Hack không đảm bảo sự an toàn tuyệt đối cho bạn bởi sự an toàn tuyệt đối không tồn tại trên Internet.  Tuy nhiên, bạn có thể khiến cho cuộc sống của các hacker và mã độc của họ gặp thật nhiều khó khăn bằng cách thực hiện những thủ thuật/mẹo này.
* Để bắt đầu: hãy giũ bỏ sự sợ hãi trước máy tính của bạn. Khả năng một hacker phải trả phí hay vận dụng những kỹ thuật cao cấp nhất để tấn công bạn là không cao dù rằng mỗi người trong chúng ta đều có thể đã, đang và sẽ là nạn nhân của tội phạm mạng. Hầu hết các mối đe dọa bắt nguồn từ thực tế là nhiều người dùng máy tính thiếu kiến thức cơ bản về Internet và máy tính, từ đó có thể bị lợi dụng để tấn công họ. Vì thế, chúng ta hãy cập nhật những thông tin quan trọng và được cập nhật này. 👍

## Hacker là ai

![image](https://user-images.githubusercontent.com/526959/47335989-0fab2100-d6b8-11e8-8b4c-fc1e7b345f6b.png)

* Các hacker thường khai thác các lỗ hổng tồn tại trên môi trường Internet hoặc của các thiết bị mà chúng ta sở hữu. Trong bài viết này, ta đề cập hai dạng hacker chính sau: white hat và black hat. Các hacker white hat 🤠 tìm kiếm (và thi thoảng công bố) các lỗ hổng bảo mật để các công ty sửa chữa chúng, giúp cho Internet phần nào được an toàn hơn.
* Khi các hacker được nhắc đến trên truyền thông, đó thường là các hacker black hat 😈. Đây là các hacker không có ý định tốt, người mà có thể đang tìm kiếm cách để đánh cắp tiền hoặc chiếm quyền truy cập vào các thiết bị để theo dõi bí mật chúng ta (gián điệp máy tính). Họ có thể quan tâm đến các file nhạy cảm, như các bức ảnh nude của bạn hoặc bản copy, thông tin chứng minh thư, passport của bạn.
* Cũng có những hacker cố gắng truy cập vào các thiết bị của người khác vì niềm vui làm được việc này (for fun). Đây hầu hết là những hacker tinh nghịch trẻ tuổi. Mặc dù họ có những động cơ ngây thơ/vô tư, những hành động của họ cũng có thể để lại các mối nguy hại.
* Cuối cùng, một số **hacker làm việc cho các chính quyền**. Những hacker này được thuê bởi các dịch vụ bí mật 🕵️ hay công an 👮 (an ninh, cảnh sát) là **dạng hacker nguy hiểm nhất**. Họ thường tấn công vào các lực lượng khủng bố, tội phạm và các đối tượng, tổ chức thù địch.

## Các hacker thường vào được các thiết bị, máy tính và tài khoản online của bạn như thế nào?
* Các hacker thường bắt đầu bằng cách tìm cách đánh cắp mật khẩu (password) của bạn. Nhiều lúc, bạn không thể kiểm soát được việc này. Nếu một website mà bạn sử dụng bị hack thành công, các hacker có thể lấy được thông tin password và thử sử dụng thông tin password đó để đăng nhập vào các tài khoản khác của bạn, ví dụ như Gmail.
* Bạn có thể đã đưa mật khẩu của bạn cho người khác dù bạn không có chủ ý. Việc này được thực hiện thông qua lừa đảo (phishing), là một dạng lừa đảo thông qua Internet của giới tội phạm tìm cách lấy thông tin đăng nhập một dịch vụ nào của bạn. Khả năng cao là bạn đã từng nhận được một email lừa đảo trước đây. Đó cũng có thể là một tin nhắn giả về tài khoản ngân hàng của bạn bị khóa hay một nhắc nhở về một khoản thanh toán không tồn tại mà bạn chưa trả.
* Các hacker cũng sử dụng các đính kèm email (email attachments). Khi bạn mở một file đính kèm chứa mã độc, máy tính của bạn bị lây nhiễm mã độc. Phương pháp này thường được sử dụng để lây lan ransomware: một dạng virus khiến cho thiết bị của bạn không sử dụng được bằng cách khóa khả năng sử dụng các file của bạn. Các hacker sẽ yêu cầu bạn trả tiền đổi lại việc bạn được phục hồi khả năng truy cập các file của bạn.
* Các virus - thường được gọi với tên malware (phần mềm độc hại, mã độc) cũng thường được phát tán qua việc tải các nội dung từ torrent lậu hoặc các file cài đặt cho một phần mềm bạn muốn sử dụng. Bạn có thể nghĩ rằng bạn đang tải một bộ phim hoặc một phần mềm giúp cho máy tính của bạn nhanh, sạch, ngăn nắp nhưng thực tế là bạn đang tự làm hại mình qua việc tự cài đặt mã độc.
* Một virus cũng có thể vào được máy tính của bạn thông qua các quảng cáo online hoặc các website đã bị hack. Ngay cả những website mà bạn tin tưởng cũng có thể đang phát tán mã độc mà chủ nhân các website này không hay biết. Nếu bạn không cập nhật phần mềm và máy tính của bạn, bạn đang có nguy cơ bị lây nhiễm các dạng mã độc này.
* Các hacker cũng lây nhiễm máy tính của bạn thông qua các thiết bị di động flash drive. Phương pháp này dù ít thịnh hành hơn, nhưng nó cũng tạo một nguy cơ đáng kể. Đó có thể là một ổ cứng di động mà bạn vừa tìm thấy ở công ty hay ai đó gửi cho bạn. Bất cứ ai có ý định hại bạn có thể truy cập vật lý vào máy tính của bạn nếu như bạn bỏ máy tính của mình đi toilet mà không khóa truy cập.

## Nhập môn

![image](https://user-images.githubusercontent.com/526959/47344315-63c2ff00-d6d2-11e8-92d9-60d322fc6d0b.png)

* Bây giờ bạn đã biết các hacker và làm thế nào mà họ chiếm được quyền truy cập, bạn có thể bắt đầu thực hiện một số thủ thuật 💡. Đây là những điều rất cơ bản: một danh sách đơn giản những biện pháp mà mọi người nên thực hiện.

### Cập nhật phần mềm
* Rất nhiều người xem việc cập nhật phần mềm là hoạt động tốn thời gian. Trong một số trường hợp, điều này đúng, nhưng cũng cần biết rằng hoạt động này cũng là một trong những hoạt động bảo vệ quan trọng nhất ❗ để sử dụng chống lại tội phạm mạng. Nhiều vụ tấn công được thực hiện thành công chỉ vì các nạn nhân đã sử dụng các phần mềm không được cập nhật các bản vá bảo mật. Những phần mềm này khi ấy chứa nhiều các lỗ hổng bảo mật cần được sửa chữa qua các bản cập nhật/bản vá bảo mật.
  * Đối với hầu hết các phần mềm: Một phần mềm (software) càng cũ thì càng dễ dàng cho các hacker chiếm quyền kiểm soát.
* Phần mềm được chạy trên nhiều dạng thiết bị chạy các điều hành khác nhau như: Windows hay MacOS trên máy tính để bàn hoặc laptop, và Android hay iOS trên các thiết bị di động. Ngay cả một router và các thiết bị thông minh khác trong nhà của bạn cũng chạy phần mềm. Đảm bảo rằng bạn kiểm tra những bản cập nhật này hàng tuần, và cài đặt chúng ngay khi có thể ⏰. Trong một số trường hợp, các bản cập nhật được cài đặt một cách tự động. Hệ điều hành Windows có bản quyền, MacOS và trình duyệt Chrome hỗ trợ chức năng cập nhật tự động này.
* Việc cập nhật các ứng dụng, phần mềm được cài đặt trên máy tính của bạn như trình duyệt, trình đọc file PDF, và Microsoft Office có bản quyền là rất quan trọng. Bạn sẽ thường nhận được các thông báo của các phần mềm này nếu đã có các bản cập nhật bảo mật.

### Password
* Ngày nay, bạn gần như sẽ cần một tài khoản để sử dụng các dịch vụ chuyên biệt cho người dùng của các website hay ứng dụng, để sử dụng tài khoản này, bạn sẽ cần đến password (mật khẩu). Là con người, chúng ta sẽ có trở ngại trong việc nhớ nhiều các password khác nhau, vì thế chúng ta thường có xu hướng sử dụng một password cho nhiều account khác nhau.
* Trong khi việc sử dụng chung password giúp cho bạn rất dễ nhớ, việc này cũng **rất rất nguy hiểm** ⚠️. Nếu một hacker có được mật khẩu trang Spotify của bạn, bạn sẽ không muốn hacker đó có thể truy cập đến tài khoản ngân hàng của bạn. Và nếu như bạn chia sẻ password Netflix của bạn với một người bạn, người đó không nên có thể sử dụng nó để đăng nhập vào tài khoản Gmail hay Facebook của bạn.
* Đấy là tại sao việc sử dụng mật khẩu khác nhau cho các website, ứng dụng và dịch vụ khác nhau là rất quan trọng. Chỉ thay đổi một chữ số 1️⃣ hay 1 chữ cái 🅰️ sẽ không cải thiện việc này. Bởi vì những dạng thay đổi này quá dễ đoán. May mắn là đã có một giải pháp tiện lợi cho vấn đề này: sử dụng các **phần mềm quản lý mật khẩu** (**password managers**).

### Phần mềm quản lý password
* Một phần mềm quản lý tất cả các password của bạn trong một kho kỹ thuật số 🔑 có khóa bảo vệ và đảm bảo an toàn cho chúng bằng một password mạnh là password chính duy nhất. Bằng cách này, bạn chỉ phải nhớ một password để truy cập tất cả tài khoản của bạn. Những ứng dụng này có thể dễ dàng sinh ra các password phức tạp, như 6ur7qvsZpb0ZkcuSW1u!V8ng!L^lb . Một password như vậy không thể đoán được và vô cùng khó/không khả thi để bẻ khóa trong thời gian hữu hạn (1 đời người).
* Các phần mềm quản lý password có thể tự động điền thông tin đăng nhập khi bạn truy cập một website bạn đã từng sử dụng và có password được lưu. Chỉ riêng chức năng đã giúp bảo vệ bản khỏi rất nhiều các tấn công. Nếu như địa chỉ website không chính xác, ví dụ như wellsfargo.mybanklogin.com, ứng dụng quản lý password sẽ không điền thông tin đăng nhập website ngân hàng Wells Fargo vào. Bạn cũng có thể sử dụng một ứng dụng quản lý password để lưu trữ các ghi chú (note), ví dụ như các mã đăng nhập, các khóa bí mật và câu trả lời cho các câu hỏi bí mật.
* Một số ứng dụng quản lý password tốt: LastPass, 1Password, Bitwarden và KeePass. Nếu bạn chưa bao giờ sử dụng một ứng dụng quản lý password trước đây, hãy thử sử dụng phiên bản miễn phí của LastPass cho một khởi đầu tốt để làm quen.

#### LASTPASS (FREE)
* [LastPass](https://www.lastpass.com/) là ứng dụng quản lý mật khẩu có rất nhiều chức năng, bao gồm một ứng dụng mở rộng cho trình duyệt web để sinh mật khẩu ngẫu nhiên và điền thông tin đăng nhập cho bạn. LastPass có các ứng dụng tốt cho các hệ điều hành cơ bản thường gặp và vẫn hoạt động tốt ngay cả với phiên bản miễn phí. Phiên bản có phí cho bạn một gigabyte để lưu trữ tài liệu nhạy cảm và lựa chọn để chia sẻ (share) password với những người dùng LastPass khác.

![image](https://user-images.githubusercontent.com/526959/47352432-12237000-d6e4-11e8-8798-e710d014d749.png)

#### 1PASSWORD (3 USD/THÁNG)
* [1Password](https://1password.com/) nổi tiếng với thiết kế đẹp và được tối ưu cho việc sử dụng trên các thiết bị của Apple, như iPhone và Macbook. Ứng dụng này có một sứng dụng mở rộng trình duyệt (extension) [1Password X](https://support.1password.com/getting-started-1password-x/) cho phép sinh ra các password ngẫu nhiên và điền chúng vào khi bạn truy cập các website mà bạn có thể đăng nhập. Khi đăng ký dịch vụ của 1Password, bạn sẽ nhận được một khóa bảo mật đặc biệt ([khóa bí mật](https://support.1password.com/secret-key-security/)), bạn cần dùng khóa này và Master Password của bạn để có thể truy cập tài khoản của bạn.

![image](https://user-images.githubusercontent.com/526959/47352478-2bc4b780-d6e4-11e8-933f-35cbfbf92870.png)

#### BITWARDEN (FREE)
* [Bitwarden](https://bitwarden.com/) đã trở nên khá thông dụng những năm gần đây. Đây là 1 ứng dụng hoàn toàn mở, có thể cài đặt trên nhiều nền tảng và có thể sử dụng miễn phí. Bạn có thể chia sẻ password với vợ/chồng hay người trong gia đình, một chức năng mà bạn phải trả phí để sử dụng trong hầu hết các ứng dụng quản lý password khác. Nếu bạn muốn chia sẻ password với hơn một người, bạn sẽ phải trả phí 1 USD một tháng, đồng thời dịch vụ cũng sẽ cung cấp cho bạn 1 gigabyte chứa dữ liệu cho các file của bạn. Những người dùng rành kỹ thuật có thể tự vận hành hạ tầng Bitwarden cho riêng mình.

![image](https://user-images.githubusercontent.com/526959/47355448-975e5300-d6eb-11e8-8d8e-397167538043.png)

#### KEEPASS (FREE)
* [KeePass](https://keepass.info/) được xem là ứng dụng quản lý password an toàn nhất, bởi vì nhiều chuyên gia bảo mật sử dụng ứng dụng này và đã tham gia làm cho nó an toàn hơn với kiến thức chuyên môn của họ. Điểm hạn chế là ứng dụng này nhìn khá cũ (old-fashioned), giống như một ứng dụng Windows XP. May mắn là cộng đồng sử dụng KeePass đầy những lập trình viên đầy đam mê đã làm những ứng dụng đẹp hơn với KeePass, ví dụ [MacPass for MacOS](https://macpassapp.org/). Một lựa chọn tốt khác là [KeePassXC](https://keepassxc.org/), về nhiều mặt là một phiên bản tốt và đầy đủ hơn cho KeePass, và cũng thường xuyên được cập nhật bởi một nhóm các lập trình viên đầy nhiệt huyết.

![image](https://user-images.githubusercontent.com/526959/47356192-86164600-d6ed-11e8-9735-f2623a723355.png)

Bạn có thể nghĩ: liệu một cái tủ khóa điện tử có an toàn hay không? Đây là một câu hỏi hay, và là một mối quan ngại có thể hiểu được. Ví dụ: LastPass đã bị hack [2](https://blog.lastpass.com/2015/06/lastpass-security-notice.html/) [lần](https://blog.lastpass.com/2017/03/security-update-for-the-lastpass-extension.html/). Dù vậy, các password chưa bao giờ bị đánh cắp, bởi vì chúng được lưu trữ trong một kho kỹ thuật số rất an toàn. 

### Mật khẩu mạnh
* Các website và ứng dụng thường yêu cầu bạn sử dụng mật khẩu có chữ và số. Nhưng một password như thế nào là 1 password mạnh? Nhiều người xem ```P@ssword007``` là 1 password mạnh nhưng trong thực tế, password này khá dễ crack 🔨 đối với các hacker. Đó là lý do tại sao bạn nên cân nhắc sử dụng passphrase (cụm password) thay vì các password được tạo với 1 từ đơn giản.
* Cụm password dài nhưng dễ nhớ, là 2 điều kiện tiên quyết cho một password mạnh. Một passphrase như ```I eat 2 whole pizzas every week``` thì dễ nhớ và khá khó để để crack. Đừng ngần ngại sử dụng các khoảng trắng trong các password của bạn; đây là 1 lựa chọn mà chúng ta thường bỏ qua.
* Bạn cũng có thể tạo một password bằng cách đặt những từ ngẫu nhiên lại với nhau với phương pháp [Diceware](http://world.std.com/~reinhold/dicewarefaq.html) với [1 wordlist tốt](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) [đủ lớn](https://raw.githubusercontent.com/heartsucker/diceware/develop/wordlists/en_US/wordlist-8192.txt). Diceware hiện tại gần như là phương pháp an toàn nhất để tạo một password mà bạn có thể nhớ được.

### Tóm lược về cách tốt nhất để lưu trữ password
* Sử dụng một phần mềm quản lý password ([password manager](#ph-n-m-m-qu-n-l-password)), nên là 1 trong các phần mềm được giới thiệu ở trên.
* Sử dụng một [passphrase](#m-t-kh-u-m-nh) hoặc phương pháp Diceware để tạo password của bạn.
* Viết xuống password quản lý mật khẩu của bạn (master password/manager password để đăng nhập password manager) và giữ nó ở một nơi an toàn, đảm bảo rằng bạn không bao giờ mất khả năng truy cập password manager.
* Sử dụng password manager để sinh ra các password có độ dài **từ 20 ký tự trở lên** và để password manager lưu trữ những password này cho bạn.

### Những cách thức lưu giữ password không an toàn khác (iCloud Keychain, lưu mật khẩu trong trình duyệt, sổ tay password)
#### ICLOUD KEYCHAIN
* iCloud Keychain là 1 cách lưu trữ password nếu bạn chỉ tập trung sử dụng các sản phẩm của Apple 🍏. Keychain có thể sinh password và tự động điền password khi bạn cần đến chúng. Chức năng của iCloud Keychain khá là giới hạn so với các ứng dụng quản lý password khác. Nếu sử dụng iCloud Keychain ít nhất bạn cần sử dụng một password mạnh và xác thực 2 yếu tố (đa nhân tố) cho tài khoản iCloud.

![image](https://user-images.githubusercontent.com/526959/47401825-0334d000-d76d-11e8-87fc-0cb5362d6dd6.png)

#### Lưu trong trình duyệt
* Các trình duyệt như Chrome và [Firefox](https://support.mozilla.org/en-US/kb/use-master-password-protect-stored-logins) cho phép lưu password trong trình duyệt nhưng sử dụng một ứng dụng quản lý password là 1 lựa chọn tốt hơn.

#### Sổ tay password
* Giấy và bút 📝 có thể được dùng để lưu giữ password. Hãy đảm bảo rằng bạn tạo ra các password duy nhất khác nhau và lưu trữ chúng cẩn thận. Và tạo ra một bản copy trong một kho vật lý mà bạn giữ làm backup. Nếu lo lắng người khác có thể đọc được password ghi trên giấy của mình, bạn hãy chú ý không để mọi người có thể tiếp cận đến sổ tay của bạn. Một thủ thuật hữu dụng nữa là bạn có thể thêm một từ cố định vào password của bạn mà bạn sẽ không ghi ra từ này vào sổ tay password. Chỉ đơn giản là nhớ nó. Nếu ai đó có thể tiếp cận sổ tay password của bạn, ít nhất họ không thể sử dụng password nào bạn đã viết ra, bởi vì chúng đã thiếu mất một thành phần quan trọng được nhớ bằng não của bạn.

![image](https://user-images.githubusercontent.com/526959/47403116-8c9ad100-d772-11e8-93ba-7b43aab0bb71.png)

### Cập nhật danh sách những password của bạn đã bị đánh cắp
* Dù cho password của bạn có rất mạnh đến đâu đi nữa, nó cũng có thể bị đánh cắp. Chính vì vậy, bạn cần kiểm tra xem các password của bạn đã bị đánh cắp bởi các hacker chưa. Bạn có thể sử dụng website [Have I Been Pwned](https://haveibeenpwned.com/) hỗ trợ bạn theo dõi các website đã bị hack mà tài khoản của bạn bị ảnh hưởng và sẽ cảnh báo bạn khi có thông tin xuất hiện. Chỉ với một click chuột, bạn có thể biết liệu có tài khoản nào của bạn đã bị xâm nhập. Bạn nên thường xuyên làm việc kiểm tra này để giữ an toàn cho tài khoản của bạn.
* Nếu bạn đăng ký với website [Have I Been Pwned](https://haveibeenpwned.com/) , bạn sẽ nhận được **thông báo** 🔔 mỗi khi hệ thống website này phát hiện email của bạn nằm trong danh sách các file chứa thông tin tài khoản bị đánh cắp. Bằng cách này, bạn sẽ biết chính xác những password nào của mình đã bị đánh cắp trong các sự cố đó, dựa vào thông tin dịch vụ hay website đã bị hacker xâm nhập. Nếu [Have I Been Pwned](https://haveibeenpwned.com/) tìm thấy email của bạn nằm trong các file bị đánh cắp, bạn nên thay đổi ngay password tương ứng của bạn. Nếu bạn làm được việc này, mối hiểm họa lớn nhất, một hacker đăng nhập sử dụng password của bạn đã được giảm đi đáng kể.

### Xác thực Hai Yếu Tố (Đa Nhân Tố)
* Để giới hạn làm giảm mức độ ảnh hưởng khi một password bị đánh cắp, bạn nên sử dụng xác thực 2 yếu tố (2FA, đa nhân tố) là một phương pháp bảo mật hiện đại.
* Bạn có thể kích hoạt xác thực 2 yếu tố  qua các dịch vụ mà bạn sử dụng, nếu như họ hỗ trợ xác thực 2 yếu tố. Sau khi đăng nhập với username và password, kể từ bây giờ bạn sẽ phải thực hiện thêm một bước thứ 2 khi đăng nhập. Thông thường, dịch vụ của website sẽ yêu cầu bạn nhập vào mã được sinh cho bạn qua một smartphone (điện thoại thông minh) bằng các ứng dụng authentication hoặc tin nhắn từ dịch vụ.

![image](https://user-images.githubusercontent.com/526959/47403613-53636080-d774-11e8-9a23-192c3e486458.png)

* Tại sao nên thực hiện thêm bước này chi cho rắc rối? Nếu một hacker tìm cách có được thông tin đăng nhập của bạn, người đó sẽ cần phải lấy được cả mã đăng nhập được tạo ra cho điện thoại của bạn ngay khi hacker thử đăng nhập tài khoản của bạn. Việc này tạo khó khăn cho hacker vì anh ta cần truy cập điện thoại của bạn hoặc đánh cắp mã xác thực được gửi đến điện thoại của bạn ⛔. Xác thực hai yếu tố cũng cảnh báo cho bạn những cố gắng truy cập thâm nhập tải khoản của bạn, trong trường hợp password của bạn bị đánh cắp và bạn nhận được thông báo của dịch vụ website về việc có người cố gắng truy cập tài khoản với password của bạn. Nhờ vậy, bạn sẽ biết được có ai đó đã cố gắng xâm nhập tài khoản của bạn. Bạn có thể vào website [Two Factor Auth List](https://twofactorauth.org/) để kiểm tra các dịch vụ, ứng dụng, website nào đã hỗ trợ xác thực hai yếu tố (đa nhân tố). [Google](https://support.google.com/accounts/answer/9096865), [Apple](https://support.apple.com/en-us/HT204915), [Facebook](https://www.facebook.com/help/148233965247823), [Instagram](https://help.instagram.com/566810106808145), [WhatsApp](https://faq.whatsapp.com/en/android/26000021/) và [Dropbox](https://www.dropbox.com/en/help/security/enable-two-step-verification) đều đã là các dịch vụ hỗ trợ các chức năng xác thực hai yếu tố (đa nhân tố).

#### Mã xác thực qua tin nhắn điện thoại
* Nhận mã xác thực qua tin nhắn điện thoại rất đơn giản: bạn link số điện thoại của bạn vào một dịch vụ online và điền mã xác thực được gửi đến điện thoại của bạn tương ứng với website hay app đó. Chú ý là các hacker có thể lấy được các mã xác thực đăng nhập bằng cách can thiệp vào quá trình nhận tin nhắn điện thoại của bạn 💬 hoặc sử dụng những kỹ thuật lừa đảo. Vì vậy, nhiều chuyên gia đã khuyến nghị không sử dụng xác thực 2 yếu tố qua tin nhắn điện thoại mà thay thế bằng phương thức xác thực 2 yếu tố khác an toàn hơn như sử dụng MÃ XÁC THỰC QUA CÁC ỨNG DỤNG AUTHENTICATOR chẳng hạn.

#### MÃ XÁC THỰC QUA CÁC ỨNG DỤNG AUTHENTICATOR
* Một cách an toàn cho xác thực hai yếu tố là sử dụng một ứng dụng authenticator. Những ứng dụng này cho phép bạn scan một QR-code là một barcode để scan bằng camera của smartphone của bạn. Mã QR-code được cung cấp bởi dịch vụ mà bạn muốn bảo mật. Sau khi scan QR-code, một mã bảo mật sẽ xuất hiện trên màn hình trong vòng 30 giây, ngay sau đó một mã khác sẽ được sinh ra. Những mã ngẫu nhiên này cho phép bạn xác thực việc truy cập của bạn, để dịch vụ online biết rằng bạn chính là người đang cố gắng truy cập tài khoản của bạn. [1Password](https://1password.com/), [LastPass Authenticator](https://lastpass.com/auth/), [Authy](https://authy.com/) và [Google Authenticator](https://support.google.com/accounts/answer/1066447) đều sinh ra các mã như vậy. Chú ý rằng khi sử dụng Google Authenticator, nếu bạn để mất điện thoại của bạn hoặc nếu ứng dung Google Authenticator bị reset, bạn sẽ mất tất cả các mã xác thực đăng nhập trên điện thoại đó. Những ứng dụng authenticator khác được nhắc ở trên cho phép bạn đồng bộ các mã xác thực đăng nhập này trên tất cả các thiết bị mà bạn sử dụng ứng dụng đó.

### Kiểm tra biểu tượng ổ khóa (và các yếu tố khác)
* Biểu tượng ổ khóa 🔒 trên thanh địa chỉ của trình duyệt cho bạn biết bạn đang sử dụng một kết nối được mã hóa. Điều đó có nghĩa rằng thông tin mà bạn gửi vào website như password của bạn, thông tin credit card, được gửi đi theo một phương thức an toàn mà hacker sẽ không dễ dàng đọc trộm/nghe lén trên đường truyền được. Hãy đảm bảo rằng bạn chỉ gửi thông tin nhạy cảm trên các website mà có hiện ra biểu tượng ổ khóa này trên thanh địa chỉ của trình duyệt web. Nếu địa chỉ một website bắt đầu với ```https://```, điều đó có nghĩa là website này tương đối an toàn.

![image](https://user-images.githubusercontent.com/526959/47407356-e5736500-d784-11e8-9219-36e581574137.png)

* Cũng cần chú ý là biểu tượng ổ khóa không có nghĩa rằng bạn nên tin tưởng một website bạn đang truy cập 🚫. Nhiều website lừa đảo được thiết kế để đánh cắp thông tin đăng nhập của bạn cũng dùng biểu tượng ổ khóa này để gia tăng sự tin tưởng của bạn. Hãy chú ý đặc biệt vào địa chỉ website và kiểm tra rằng địa chỉ đó có chính xác hay không. Ví dụ:
  * **Chính xác**: https://www.facebook.com (facebook.com là tên miền chính)
  * **Sai**: https://www.facebook.tech (.tech không phải là phần mở rộng tên miền đúng)
  * **Sai**: https://facebook.login.net (login.net là tên miền chính ở đây)
  * **Sai**: https://www.faceb00k.com (2 chữ o đã được thay thế bằng 2 chữ số 0)

### Thực hiện backup
* Một bản backup (sao lưu) cho phép bạn truy cập các file của bạn khi bạn gặp các sự cố? Điều gì sẽ xảy ra nếu máy tính của bạn đột ngột bị hỏng? Những hình ảnh 📷, video 📹 và các tài liệu nào 📃 bạn **thực sự cần lưu trữ** và những file nào bạn cần cho công việc thường trực của bạn? Đây là những file mà bạn nên backup.
* Backup là 1 biện pháp bảo vệ cho những file quan trọng của bạn, ngay cả khi máy tính của bạn bị hỏng, điện thoại của bạn bị đánh cắp hoặc ransomware khiến cho máy tính của bạn không sử dụng/truy cập được. Một bản backup sẽ giúp bạn phục hồi công việc một cách nhanh chóng.
* Chúng tôi khuyến nghị bạn nên giữ 2 bản **backup online và offline**. Bạn có thể tạo các bản backup online với một dịch vụ cloud ☁️ như [Dropbox](https://db.tt/MOb89WKAbn), [Degoo](https://cloud.degoo.com/drive-na6hsumn9boh), [pCloud](https://my.pcloud.com/#page=register&invite=ERR3ZN7n5C7) và những bản backup offline sử dụng ổ cứng rời gắn ngoài. Hãy đảm bảo rằng bạn kiểm tra thường xuyên định kỳ các file được lưu trữ vẫn ở đúng vị trí của chúng và vẫn hoạt động tốt.

### Nhận dạng lừa đảo
* Các tấn công dựa trên lừa đảo kỹ thuật số thường khá dễ để nhận biết. Lấy ví dụ một email giả như được gửi từ Bank of America, email này bảo rằng debit card đã bị khóa, mặc dù bạn không hề có một tài khoản đối với Bank of America 🏦. Hãy sử dụng **suy nghĩ logic** để bảo vệ bạn trên không gian mạng.
* Nhưng các email lừa đảo cũng có thể trông rất thật. Vì vậy, việc kiểm tra địa chỉ email của người gửi luôn là một việc cần thiết. Nếu người gửi sử dụng ```@bankofamerica.bankmailservice.com```, bạn sẽ biết rằng email này không thực sự được gửi bởi Bank of America. Nếu là email hợp lệ, ít nhất địa chỉ email đó nên có địa chỉ ```@bankofamerica.com```.
* Chú ý vào việc **sử dụng ngôn ngữ lạ hoặc không chuẩn xác**. Nhiều email lừa đảo chưa các lỗi văn phạm hay lỗi chính tả và chúng có bắt đầu thư một cách chung chung như ```Dear sir/madam```. Hầu hết các tổ chức biết chúng ta là ai và sẽ gọi bạn bằng tên chính xác của bạn.
* Thông thường, các email lừa đảo sẽ cố gắng **làm cho bạn hoảng sợ** 😨 ví dụ như có thể thông báo rằng tài khoản ngân hàng của bạn đã bị khóa hoặc là bạn có dư nợ chưa thanh toán cần được trả cho ngân hàng. Chúng cũng có thể bảo rằng bạn đã trúng thưởng một món gì đó 🤑. Nếu như bạn không chắc chắn về nội dung của email, hãy gọi điện đến số điện thoại chính thức (lấy từ một nguồn khác) của tổ chức được giả định đã gửi email đến cho bạn. Tuyệt đối không sử dụng số điện thoại được cung cấp trong email mà hãy tìm kiếm trên website chính thức của tổ chức đó!
* Trước khi click vào **link trong một email**, hãy luôn luôn kiểm tra tính xác thực của link đó. Bạn có thể thực hiện bằng cách đặt trỏ chuột 🖱️ lên trên link đó mà không click vào nó. Khi đó trang web mà link sẽ đưa bạn đến sẽ hiển thị trên màn hình. Bạn sẽ có thể biết được đó có phải là 1 link hợp lệ hay đây là 1 cố gắng lừa đảo bạn. Trên một thiết bị di động, bạn có thể nhấn và giữ trên link để copy link đó ra. Sau đó tạo một email và paste (dán) link đó vào body (phần nội dung) của email để đọc được toàn bộ địa chỉ web mà link đó dẫn tới.
* Nếu bạn không tin tưởng một email hay các link trong email đó, hãy sử dụng trình duyệt web để vào website chính thức của tổ chức mà email thể hiện được gửi tới từ tổ chức đó, nếu bạn có tài khoản ở tổ chức đó thì hãy **đăng nhập thử để kiểm tra bạn có nhận được tin nhắn, hóa đơn hay thông báo nào gần đây** từ tổ chức đó hay không. Bạn cũng có thể **gọi điện thoại** 📞 đến tổ chức đó để hỏi email mà bạn nhận được có phải được gửi từ tổ chức đó hay không.
* Một nguyên tắc quan trọng để thực hiện trên không gian mạng: ```Nếu một việc nào đó quá tốt để là sự thật, thì bạn cần suy xét cẩn thận về việc đó.```
* Nếu bạn có một tài khoản Google, plugin [Password Alert](https://chrome.google.com/webstore/detail/password-alert/noondiphcddnnabmjcihcjfbhfklnnep) cho trình duyệt của bạn có thể giúp ích cho bạn. Password Alert sẽ **cảnh báo bạn** khi password Google của bạn được gõ vào một trang web login giả mạo. Cài đặt plugin chính thức của Google này có thể là 1 cứu cánh, khi mà tài khoản Google và Gmail trở nên quan trọng với rất nhiều người.

### Đừng mở bất kỳ link nào bạn nhận được mà không cẩn thận kiểm tra (Don’t just click on any link)
* Một việc hầu như luôn đúng là bạn không nên click vào bất cứ link nào bạn nhận được, ngay cả khi link đó được gửi đến từ bạn bè hay đồng nghiệp của bạn. Đây là một lời khuyên tốt cho bất kỳ tình huống nào bạn có thể gặp; cho dù đó là một link nhận được trong email, qua mạng xã hội, truyền thông hay trong một tin nhắn. Một smartphone có thể bị hack khi bạn sai lầm click vào một link chứa mã độc.
* Dù vậy, bạn cũng không cần quá sợ hãi trước tất cả các link bạn nhận được. Nếu như bạn không tin tưởng link đó, hãy **kiểm tra link đó** 👓 trước tiên bằng các phương pháp được miêu tả ở trên.

### Cẩn thận với các file đính kèm và kiểm tra các file mà bạn không tin tưởng
* Hãy luôn cẩn trọng với **các file đính kèm trong các email**. Virus và mã độc thường được phát tán qua phương thức này, có thể cho phép các hacker truy cập và điều khiển thiết bị của bạn. Họ làm việc này bằng cách ẩn giấu mã độc trong một file dường như là sạch, ví dụ như một file Word.
* Các hacker cũng ẩn giấu mã độc trong các dạng file Excel, PDF, ZIP và các file thực thi được (EXE, PIF,...). Phương án tốt nhất là không mở các file Word, Excel hay các file văn bản khác trên máy tính của bạn. Bạn hãy mở các file trên bằng website [Google Docs](https://docs.google.com/). Như vậy, nếu có mã độc ẩn chứa trong các file này, máy tính của bạn sẽ không bị lây nhiễm mã độc. Ngoài ra, với các file PDF, tốt nhất bạn nên mở chúng trong trình duyệt Internet với ứng dụng mở rộng trình duyệt [PDF Viewer](https://chrome.google.com/webstore/detail/pdf-viewer/oemmndcbldboiebfnladdacbdfmadadm).
* Nếu bạn không tin tưởng một file mà bạn không thể xác thực được, bạn có thể tải nó về ⬇️ máy tính của bạn, nhưng đừng mở file đó! Sau khi tải file về, bạn có thể upload file đó lên [VirusTotal](https://www.virustotal.com/). VirusTotal là một website cho phép scan các file với nhiều antivirus engine khác nhau và cho bạn biết file đó có thể chứa mã độc hay không. Chú ý là Google và VirusTotal có thể truy cập được file của bạn sau khi bạn upload file đấy lên VirusTotal.
* Một khuyến nghị khác là bạn nên tắt đi lựa chọn ```ẩn phần mở rộng cho biết định dạng file (file extension)``` đối với hệ điều hành [Windows](https://www.howtogeek.com/205086/beginner-how-to-make-windows-show-file-extensions/) và [Mac OS X](https://www.howtogeek.com/211496/how-to-hide-files-and-view-hidden-files-on-mac-os-x/). Việc này cho phép bạn thấy ngay được phần mở rộng của file như ```.docx``` hay ```.pdf```.

### Thận trọng với mạng WiFi công cộng
* Những mạng WiFi công cộng, ví dụ mạng WiFi Starbucks, không an toàn. Các hacker có thể theo dõi thói quen truy cập của bạn và đánh cắp thông tin đăng nhập của bạn. Hãy sử dụng **kết nối 4G** để thay thế, hoặc tạo một Wi-Fi hotspot được bảo vệ với password trên điện thoại di động của bạn. Một Wi-Fi hotspot ([Android](https://support.google.com/android/answer/9059108), [iPhone](https://support.apple.com/en-us/HT204023)) cho phép laptop của bạn kết nối Internet thông qua kết nối 4G của smartphone của bạn.
* Nếu bạn thực sự cần sử dụng các mạng WiFi công cộng, hãy đảm bảo rằng bạn chỉ đăng nhập các website có hiển thị **ổ khóa** trên trình duyệt web. Các website có hiển thị ổ khóa trên trình duyệt mã hóa thông tin được gửi đi trên kết nối từ trình duyệt đến website, sẽ giảm khả năng truy cập bởi các hacker. Lời khuyên này cũng đúng với các mạng WiFi của các nhà hàng 🍟 và khách sạn 🛏️. Mặc dù các mạng WiFi này được bảo vệ với password, chúng cũng được sử dụng bởi rất nhiều người.
* Hãy chú ý đến các màn hình thông báo welcome khi kết nối đến các mạng wifi công cộng. Những trang hiển thị này có thể yêu cầu bạn cài đặt một ứng dụng, certificate hoặc một phần mềm nào đó. Kết nối đến Internet **không đòi hỏi/yêu cầu bạn làm những việc này**, vì vậy đó có thể là dấu hiệu của các hacker cố gắng truy cập đến smartphone hay laptop của bạn. Nếu bạn có các nghi ngờ, hãy hỏi nhà cung cấp mạng yêu cầu đó có chính thống hay không.
* Cuối cùng, một việc quan trọng nữa là hãy nhớ rằng mạng wifi được bảo vệ với password không nhất thiết an toàn. Những mạng wifi này cũng có thể nằm dưới sự kiểm soát của các hacker.

### Sử dụng một VPN
* Chúng tôi cũng đặc biệt khuyến nghị bạn sử dụng **VPN (kết nối mạng riêng ảo)** ngay khi bạn kết nối vào một mạng máy tính (mạng WiFi công cộng, 3G, 4G,...). Một VPN sẽ tạo một digital tunnel (đường hầm kỹ thuật số) cho các truy cập mạng của bạn. Bằng cách này, những người khác trong cùng mạng không thể thấy được những việc bạn làm trên Internet qua kết nối này, bảo vệ bạn trước các hacker.
* Hầu hết chúng ta đã từng nghe đến các VPN để truy cập Netflix. Một VPN cho phép ta đánh lừa thế giới Internet rằng **bạn đang ở một quốc gia khác** 🌎. Bằng cách kết nối đến các server VPN ở Mỹ, những người dùng VPN được truy cập đến phiên bản Netflix được cung cấp cho người dùng ở Mỹ chẳng hạn.
* Một VPN cũng rất hữu dụng nếu bạn không muốn nhà cung cấp dịch vụ mạng Internet của bạn biết được bạn đang làm gì online. Bạn có thể giữ kết nối VPN chạy liên tục để thực hiện việc này. Một thay đổi nhỏ là tốc độ Internet của bạn sẽ giảm đi một ít 🐢.
* Trong những dịch VPN tốt và tiện lợi nhất có [Freedome](https://www.f-secure.com/freedome), [iVPN](https://www.ivpn.net) và [NordVPN](https://nordvpn.com), chỉ tốn tương ứng 3, 5, 7 USD mỗi tháng. [AirVPN](https://airvpn.org) và [Mullvad](https://mullvad.net/en/) nhắm đến những người dùng nhiều kinh nghiệm.
* **Đừng bao giờ sử dụng một dịch vụ VPN miễn phí**. Những dịch vụ này nổi tiếng với việc bán thông tin cá nhân của bạn, như những website mà bạn truy cập. Nếu bạn thiếu tiền, bạn có thể tạo một tài khoản miễn phí ở 2 trang [TunnelBear](https://www.tunnelbear.com/) và [WindScribe](https://windscribe.com/?friend=4ux0nijm). Những dịch vụ này cung cấp cho bạn 500 megabyte hoặc 10 gigabyte lưu lượng truy cập mạng mỗi tháng. Lưu lượng truy cập này cũng đã đủ cho một vài trường hợp mà bạn thật sự cần dùng ở các mạng wifi công cộng.

### Đừng để thiết bị được mở một cách hớ hênh, không được khóa khi không sử dụng
* Lời khuyên này tuy có vẻ hiển nhiên, nhưng rất nhiều người để laptop của họ mở trong khi họ đang đi toilet 🚽. Bên cạnh rủi ro tài sản, dữ liệu của bạn bị đánh cắp, một người bất kỳ có thể sử dụng máy tính của bạn với ý đồ xấu trong lúc bạn không có mặt, đặc biệt là khi laptop của bạn không được đóng và khóa lại.
* Luôn luôn thiết lập laptop của bạn tự động khóa sau một khoảng thời gian thật ngắn ```(1 phút)```. Thiết bị của bạn sẽ tự động khóa nếu như bạn phải rời nó trong chốc lát. Dù vậy đây không phải là biện pháp an toàn tuyệt đối. Hãy luôn luôn cố gắng mang theo laptop của bạn đi cùng bạn nếu bạn rời chỗ ngồi hay vị trí của bạn. Ngay cả khi đó là bạn chỉ rời đi trong khoảng thời gian ngắn.

## Máy tính

![image](https://user-images.githubusercontent.com/526959/47500066-ef33c000-d88b-11e8-9676-1f68ce0c5ce0.png)

Bây giờ chúng ta chuyển qua thiết bị dễ bị hack nhất của bạn, một chiếc máy tính 💻.

### Các phần mềm antivirus vẫn hữu dụng
* Hầu hết các lây nhiễm virus xảy ra trên các máy tính Windows. Những thiết bị này đã được trang bị chương trình scan virus [Windows Defender](https://support.microsoft.com/en-us/help/17464/help-protect-my-device-with-windows-security). Windows Defender khá tốt nhưng [Kaspersky Anti-Virus](https://www.kaspersky.com/antivirus) và [Bitdefender](https://www.bitdefender.com/) (tốn 30 và 34 USD mỗi năm) dễ dàng vượt qua Windows Defender.
* Windows Defender có một chức năng bảo vệ những thư mục quan trọng của bạn khỏi ransomware và các phần mềm độc hại khác có thể làm hại đến các file của bạn. Chức năng này có thể được kích hoạt bằng cách vào ```Virus & threat protection -> Ransomware protection -> Controlled Folder Access```. Bạn cũng có thể thêm vào các thư mục khác, như là thư mục với những tài liệu kinh doanh quan trọng hay chứa các ảnh của gia đình bạn 👨‍👨‍👧.
* Sử dụng [HitmanPro.Alert](https://www.hitmanpro.com/en-us/alert.aspx) (35 USD mỗi năm) cũng được chúng tôi khuyến nghị. Bạn có thể chạy HitmanPro.Alert song song với chương trình scan virus của bạn. Nó sẽ bảo vệ bản khỏi malware cố gắng tấn công máy tính của bạn thông qua các lỗ hổng để theo dõi việc gõ phím ⌨️ trên máy tính của bạn chẳng hạn.
* Nếu bạn sở hữu một máy Mac, bạn không cần phải cài đặt một chương trình scan virus. Hệ điều hành Mac khiến cho mã độc khó lây nhiễm lên máy tính của bạn hơn. Đó là lý do vì sao không có nhiều virus lây nhiễm trên các hệ điều hành của Apple. Nếu như bạn vẫn muốn một ứng dụng scan virus, khi đó [Kaspersky Anti-Virus](https://www.kaspersky.com/mac-security) (60 USD mỗi năm), [Bitdefender](https://www.bitdefender.com/solutions/antivirus-for-mac.html) (20 USD mỗi năm) hay [ESET Cyber Security](https://www.eset.com/us/home/cyber-security/) (30 USD mỗi năm) là những lựa chọn vững chắc.
* Việc trả phí cho các chương trình scan virus mang lại giá trị của nó. Những chương trình scan virus có trả phí thường tốt hơn và có nhiều chức năng hơn các bản miễn phí. Nếu như bạn không có khả năng trả phí cho các chương trình scan virus, bạn có thể sử dụng các phiên bản miễn phí của [Avast](https://www.avast.com/free-antivirus-download) hoặc [AVG](https://www.avg.com/en-us/free-antivirus-download).

### Kích hoạt tự động cập nhật
* Như bạn đã có thể đoán trước: việc cập nhật cho các thiết bị của bạn rất quan trọng.  Đó là lý do vì sao chúng tôi khuyến nghị hãy để các bản cập nhật cho máy tính của bạn được **tự động cài đặt**. [Windows](https://support.microsoft.com/en-us/help/12373/windows-update-faq) và [MacOS](https://support.apple.com/en-us/HT201541) hỗ trợ chức năng này, [Google Chrome](https://support.google.com/chrome/answer/95414) cũng hỗ trợ chức năng tương tự.
* Nếu phần mềm bạn dùng không hỗ trợ chức năng tự động cập nhật hay thông báo các bản cập nhật mới, hãy kiểm tra tính khả tín ✅ của thông báo có bản cập nhật này trước tiên. Các virus thường lây lan qua các thông báo, cảnh báo giả, ví dụ như là một bản update cho Adobe Flash Player. Những cảnh báo này thường xuất hiện nhan nhản khi bạn duyệt web. Nếu như bạn muốn đảm bảo rằng thông báo đó có thể tin tưởng được, bạn hãy vào chính phần mềm đó và kiểm tra thủ công xem liệu đã có một bản cập nhật hay chưa.

### Sử dụng Google Chrome với 3 ứng dụng mở rộng trình duyệt sau
* Hiện nay, [Google Chrome](https://www.google.com/chrome/) là trình duyệt an toàn và thân thiện nhất với người dùng. [Firefox](https://www.mozilla.org/en-US/firefox/new/), [Safari](https://www.apple.com/safari/) and [Edge](https://www.microsoft.com/en-us/windows/microsoft-edge) cũng là các lựa chọn tốt miễn là bạn không sử dụng Internet Explorer. Đồng thời, hãy đảm bảo là bạn đã cài đặt 3 ứng dụng mở rộng trình duyệt sau:

#### UBLOCK ORIGIN
* Ứng dụng chặn quảng cáo [uBlock Origin](https://github.com/gorhill/uBlock#installation) là một ứng dụng mở rộng trình duyệt miễn phí giúp chặn các quảng cáo và các tracker theo dõi bạn trên Internet. Ứng dụng này bảo vệ bạn khỏi các quảng cáo độc hại (malvertising): các mã độc được phát tán qua các quảng cáo online. Nó cũng giúp khóa những tổ chức và công ty có tiền sử theo dõi các hành vi duyệt web online của bạn. Trái ngược với Adblock và Adblock Plus, uBlock Origin không có mô hình kinh doanh đáng ngờ. Hãy nhớ là bằng cách sử dụng ứng dụng chống quảng cáo, bạn đang làm giảm nguồn lợi nhuận của các website thu được từ quảng cáo online. Bằng cách [đưa vào danh sách trắng (whitelisting)](https://github.com/gorhill/uBlock/wiki/How-to-whitelist-a-web-site) những website ưa thích của bạn, bạn vẫn có thể ủng hộ họ có được lợi nhuận từ quảng cáo online qua các lần truy cập web của bạn.

![image](https://user-images.githubusercontent.com/526959/47509213-d1705600-d89f-11e8-98c9-2f724ce37d2e.png)

#### HTTPS EVERYWHERE
* Ứng dụng [HTTPS Everywhere](https://www.eff.org/https-everywhere) bắt buộc trình duyệt bạn phải truy cập qua kết nối an toàn khi có thể. Nếu một hacker cố gắng can thiệp vào kết nối của bạn và gửi bạn đến website qua một kết nối không an toàn, HTTPS Everywhere sẽ ngăn chặn cố gắng này của kẻ xấu đó. Ứng dụng mở rộng trình duyệt này hoàn toàn miễn phí.

![image](https://user-images.githubusercontent.com/526959/47509239-e1883580-d89f-11e8-88c3-04a18dfeeeab.png)

#### PDF VIEWER
* Giới tội phạm rất thích ẩn giấu mã độc trong các file PDF, bởi vì Adobe Reader thường có các lỗ hổng bảo mật (một ứng dụng thông dụng cho phép bạn đọc nội dung các file PDF). Đó là vì sao sẽ tốt hơn nếu bạn mở các file PDF ngay trong trình duyệt Internet của bạn. Bạn có thể sử dụng ứng dụng mở rộng [PDF Viewer](https://chrome.google.com/webstore/detail/pdf-viewer/oemmndcbldboiebfnladdacbdfmadadm) được thiết kế cho mục đích này và hoàn toàn miễn phí. Firefox có [một lựa chọn](https://support.mozilla.org/en-US/kb/view-pdf-files-firefox) cho phép bạn tự động mở các file PDF ngay trong trình duyệt Firefox.

![image](https://user-images.githubusercontent.com/526959/47509248-e947da00-d89f-11e8-944f-8015966f36f5.png)

Hãy dành sự chú ý đến các ứng dụng mở rộng trình duyệt để nhận biết được **ứng dụng nào đã do bạn chủ động cài đặt** và **đừng cài đặt quá nhiều các ứng dụng mở rộng trình duyệt**. Các ứng dụng mở rộng trình duyệt có thể được cung cấp quá nhiều quyền và trong một số trường hợp có thể xem được nội dung bạn gõ trong trình duyệt Internet của bạn. Thật may là bạn có thể xem được danh sách các quyền mà mỗi ứng dụng có thể sử dụng đối với trình duyệt Internet bạn dùng.

### Tắt JavaScript và các macro, kích hoạt ứng dụng tường lửa (firewall)
* Các hacker thường sử dụng các chức năng đặc biệt trong các phần mềm thông dụng để lây nhiễm mã độc vào máy tính của bạn. Bằng cách tắt đi các chức năng không cần thiết, bạn sẽ có được sự an toàn hơn trên không gian mạng. Việc này bao gồm tắt đi [JavaScript trong Adobe Reader](https://helpx.adobe.com/acrobat/using/javascripts-pdfs-security-risk.html) và [tắt đi các macro trong Microsoft Office](https://support.office.com/en-us/article/enable-or-disable-macros-in-office-files-12b036fd-d140-4e74-b45e-16fed1a7e5c6). Bạn hãy tắt đi cả 2 chức năng này đi.
* Một ứng dụng tường lửa (firewall) mặt khác luôn nên được kích hoạt. Ứng dụng này sẽ bảo vệ bạn trước các tấn công từ bên ngoài. Hãy kích hoạt firewall trên [MacOS](https://support.apple.com/en-us/HT201642) và luôn trên cả router của bạn nếu router của bạn có hỗ trợ chức năng firewall. Tường lửa của hệ điều hành Windows hầu như đã được kích hoạt mặc định (nếu như bạn sử dụng Windows có bản quyền). Nếu bạn cần bảo vệ bổ sung, hãy tham khảo thêm ứng dụng [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html) trên MacOS và [GlassWire](https://www.glasswire.com/) trên Windows. Những ứng dụng này sẽ theo dõi 🔎 các phần mềm truy cập ra Internet trên máy tính của bạn.

### Tránh sử dụng Flash
* Flash từng được sử dụng như là một công nghệ quan trọng trong xem các video và chơi game trong trình duyệt Internet 🎮, tuy nhiên ứng dụng này đã trở nên lỗi thời ở hiện tại, và khiến cho nó trở nên **nguy hiểm** khi dùng nó. Lựa chọn tốt nhất là bạn tránh cài đặt Flash. Nhiều trình duyệt Internet đã mặc định tắt ứng dụng Flash và yêu cầu bạn kích hoạt thủ công. Bạn chỉ nên kích hoạt Flash ở website nào mà bạn hoàn toàn tin tưởng, và có yêu cầu đặc biệt bạn làm thế.
* Hầu hết các website sử dụng công nghệ tốt hơn ở thời điểm hiện nay, như là HTML5, để hiển thị các nội dung cho phép tương tác như các video, game. Công ty đã tạo ra Flash, Adobe, sẽ chính thức ngừng hỗ trợ Flash kể từ năm 2020 và đã chính thức khuyến nghị ngừng sử dụng Flash ngay từ bây giờ.

### Kiện toàn bảo mật router của bạn
* Nhiều người gặp khó khăn trong việc cấu hình các router, thiết bị này cho phép bạn truy cập Internet. Điều này hoàn toàn dễ hiểu: các router hơi khó vận hành 😕. Mỗi router hoạt động khác nhau, nên bạn sẽ cần tìm kiếm online bản hướng dẫn sử dụng (manual). Những hướng dẫn sử dụng này sẽ giúp bạn thực hiện các thủ thuật sau:
  * Kiện toàn bảo mật mạng WiFi của bạn bằng cách thiết lập lựa chọn bảo vệ với ```WPA2-AES```, sử dụng một mật khẩu dài hoặc một passphrase và tắt đi chức năng WiFi Protected Setup (```WPS```).
  * Tắt đi chức năng ```UPNP```. Công nghệ này không an toàn và cho phép truy cập vào mạng của bạn và các thiết bị được kết nối dễ dàng hơn.
  * Cập nhật phần mềm trên router của bạn.
  * Tạo một **mạng dành cho khách** (guest network) với một password dành cho các khách đến nhà bạn và các thiết bị thông minh khác, ví dụ như các camera an ninh.
  * Đảm bảo rằng tên của mạng của bạn **không dễ dàng nhận diện đây là mạng của bạn hay của nhà bạn**. Đừng đặt tên nó kiểu như Gia Đình Johnson chẳng hạn.
  * Hãy cẩn thận với chức năng ```port forwarding```: bạn chỉ forward các port mà bạn biết chắc rằng thật sự cần thiết.

### Các thiết bị ổ cứng di động và thiết bị thông minh (Flash drives and smart devices)
* Một thủ thuật thông dụng của các hacker là tìm cách để nạn nhân gắn một **thiết bị đã bị lây nhiễm mã độc** qua cổng USB vào máy tính của họ, sau đó máy tính ấy sẽ bị lây nhiễm mã độc. Hãy luôn cản thận với các thiết bị gắn qua cổng USB, cho dù đó là thiết bị bạn vô tình nhặt được ở công ty hay trên đường phố hoặc ai đó đã cho bạn như 1 món quà 🎁. Nếu như bạn không tin tưởng thiết bị đó, hãy gửi cho 1 chuyên gia xem qua nó hoặc đơn giản là bạn hãy quăng nó đi.
* Bạn cũng có thể muốn nghĩ đến mức độ bạn thực sự cần các thiết bị thông minh kia. Bạn có thực sự cần một nồi cơm điện 🍚 có khả năng kết nối Internet qua mạng WiFi nhà bạn? Hay có thật sự quan trọng để các hình ảnh con cái bạn được thu thập bởi một camera có kết nối Internet? Tất cả những thiết bị thông minh này là **các điểm yếu có thể truy cập được** mà các hacker có thể sử dụng để xâm nhập mạng của bạn. Họ có thể chiếm quyền điều khiển các thiết bị này hoàn toàn. Bạn chỉ nên mua các thiết bị thông minh mà bạn thực sự cần và nên sử dụng các thương hiệu nổi tiếng.

### Kiện toàn giao dịch ngân hàng online
* Một số người sợ hãi trong việc sử dụng thanh toán ngân hàng trực tuyến. Không cần đến mức như vậy: thanh toán ngân hàng trực tuyến đã khá an toàn những năm gần đây. Bạn có thể sử dụng website ngân hàng của bạn hay ứng dụng mobile để thanh toán chuyển tiền 💵. Trong hầu hết các trường hợp, ứng dụng mobile này là lựa chọn an toàn nhất. Nó sẽ khó cho các hacker hay tội phạm kiểm soát được các ứng dụng này trên các phiên bản được cập nhật cho Android và iOS.

### Xóa các file
* Các file được xóa theo cách thông thường thường có thể bị phục hồi bởi các phần mềm chuyên dụng 🧐. Hãy sử dụng [BleachBit](https://www.bleachbit.org/) để bảo vệ bạn. Ứng dụng này trên Windows sẽ [gỡ bỏ hoàn toàn các file](https://docs.bleachbit.org/doc/shred-files-and-wipe-disks.html) trên ổ cứng của bạn. Bạn cũng có thể sử dụng BleachBit trên MacOS hoặc sử dụng phần mềm miễn phí [Permanent Eraser](https://itunes.apple.com/nl/app/permanent-eraser/id500541921) như là một lựa chọn miễn phí.

### Che webcam của bạn và kiểm tra môi trường xung quanh bạn
* Các tội phạm máy tính có thể theo dõi bạn qua webcam của bạn. Một hacker có thể tống tiền bạn dựa trên những hình ảnh và video thân mật của bạn. Ví dụ, bạn có thể bị bí mật ghi hình trong khi đang thay đồ, thủ dâm hay đang làm tình 🍆🍑. Chỉ bằng cách che đi webcam của bạn với một mảnh băng nhỏ, bạn khiến cho webcam ấy vô dụng với bất kỳ kẻ xâm nhập nào. Có một số lựa chọn thanh lịch hơn, ví dụ bạn có thể mua [CamHatch](https://www.camhatch.com/en) (11 USD) hay [Soomz](https://soomz.io/) (10 USD cho 3 miếng che). Bạn cũng có thể tìm thấy nhiều miếng che webcam giá rẻ khác trên các shop online của Tàu ở [AliExpress](https://aliexpress.com/).
* Đồng thời hãy **chú ý đến không gian xung quanh bạn** nếu như bạn đang sử dụng laptop trên tàu hay trong một quán cafe ☕. Liệu bất kỳ ai cũng có thể thấy bạn đang gõ gì? Bạn có chắc rằng không ai có thể thấy thông tin cá nhân của bạn trên màn hình của bạn, ví dụ như một password, địa chỉ nhà hay số điện thoại? Hãy chú ý đến tình huống mà bạn đang ở trong khi bạn đang sử dụng các thiết bị của bạn nơi công cộng.

### Chọn dùng 1 Chromebook
* Nếu bạn không phải là 1 người rành kỹ thuật và chỉ muốn dùng máy tính để duyệt web, gửi email và xem video, khi ấy **Chromebook là lựa chọn an toàn nhất của bạn**. Laptop Chromebook này không chỉ rẻ mà còn rất bảo mật bởi vì nó chỉ chạy trình duyệt web Google Chrome. Việc này khiến cho các hacker khó lây nhiễm mã độc lên máy tính này. Laptop này cho phép bạn làm tất cả những việc gì mà bạn có thể làm việc với một ứng dụng duyệt web. Nếu bạn có nhiều tiền hơn thì **iPad với một bàn phím đi kèm** sẽ là một lựa chọn tốt.

![image](https://user-images.githubusercontent.com/526959/47516337-6f1f5180-d8af-11e8-9f52-d29fd498a610.png)

### Cài đặt lại máy tính của bạn định kỳ
* Hãy cài đặt lại máy tính của bạn sau mỗi 3 năm. Điều đó cũng có nghĩa là hãy backup các file của bạn 📂, hoàn toàn xóa các ổ cứng và cài đặt lại hệ điều hành ([Windows](https://support.microsoft.com/en-us/help/4000735/windows-10-reinstall), [MacOS](https://support.apple.com/en-us/HT204904)). Việc này sẽ giúp cho máy tính của bạn nhanh hơn và gỡ bỏ các phần mềm dư thừa hay có khả năng chứa mã độc hại.

## Điện thoại và máy tính bảng

![image](https://user-images.githubusercontent.com/526959/47517016-1e105d00-d8b1-11e8-9f2c-8228c23abf54.png)

Thiết bị smartphone 📱 là thiết bị quan trọng nhất đối với cuộc sống của nhiều người, đó là lý do tại sao việc kiện toàn bảo mật cho smartphone là vô cùng quan trọng, cho dù bạn sử dụng thiết bị Android hay iPhone.

### Mua 1 iPhone
* Các điện thoại iPhone nhìn chung là an toàn hơn các điện thoại Android. Đó là lý do tại sao những người có nhiều rủi ro bị hack như các luật sư và các nhà chính trị 👴 thường sử dụng iPhone. Các iPhone cũng được đảm bảo được nhận các bản cập nhật trong 5 năm sau khi chúng được phát hành.
* Điện thoại Android an toàn nhất hiện nay là các điện thoại Pixel (trước đây có tên là Nexus), được làm bởi Google. Google đã có [những nỗ lực](https://android-developers.googleblog.com/2017/05/here-comes-treble-modular-base-for.html) phát triển hệ điều hành Android để các nhà sản xuất điện thoại như Samsung, Huawei và OnePlus có thể phát hành các bản cập nhật bảo mật nhanh hơn nhiều trước đây.

### Cập nhật ngay khi bạn có thể
* Một thủ thuật thường xuyên lặp lại trong danh sách: luôn luôn cập nhật các thiết bị di động của bạn **ngay khi bạn có thể** ⏰. Các bản cập nhật vá các lỗ hổng bảo mật cho phép các hacker xâm nhập vào smartphone hay máy tính bảng của bạn. Đồng thời hãy thường xuyên cập nhật các ứng dụng của bạn. Những ứng dụng này cũng chứa các lỗ hổng bảo mật có thể cho phép các hacker truy cập các thông tin cá nhân của bạn.

### Kích hoạt mã hóa
* Mã hóa giúp cho dữ liệu của bạn, như các tin nhắn và các hình ảnh được lưu trong kho kỹ thuật số được bảo vệ bởi các khóa bảo mật 🔑. Tất cả các điện thoại iPhone và Android có chức năng mã hóa được mặc định bật lên, nhưng một số điện thoại Android vẫn có thể yêu cầu bạn bật chức năng mã hóa lên một cách thủ công. Lựa chọn kích hoạt chức năng mã hóa có thể được tìm thấy bằng cách vào ```Settings > Security```.
* Điều gì sẽ xảy ra nếu như ai đó lấy điện thoại của bạn và kết nối nó vào một máy tính? Mã hóa đảm bảo người này không thể xem được nội dung các log chat và các bức ảnh của bạn. Những nội dung này chỉ có thể xem được nếu như passcode chính xác được nhập vào, đây chính là chìa khóa vào kho kỹ thuật số của bạn. Đó cũng là lý do tại sao sử dụng 1 passcode để khóa thiết bị di động khi bạn không sử dụng chúng là rất quan trọng.

### Sử dụng passcode với ít nhất 6 chữ số và ứng dụng scan vân tay
* Bằng cách sử dụng một passcode, bạn đã ngăn những người khác truy cập vào điện thoại hay máy tính bảng của bạn. Hãy chọn một passcode có 6 chữ số mà chỉ có bạn biết và không sử dụng một passcode đơn giản như ```0-0-0-0-0-0```, ```1-2-3-4-5-6``` hay ```1-1-2-2-3-3```. Bạn cũng không nên sử dụng ngày tháng năm sinh 🎂, tương tự với các tổ hợp thông tin cá nhân khác. Các điện thoại iPhone và Android cho phép kích hoạt chức năng tự động xóa tất cả các nội dung trên điện thoại nếu như mã đăng nhập sai được gõ vào hơn 10 lần. Chức năng này hoạt động như là một phương pháp bảo mật bổ sung, tuy nhiên nó cũng khá rủi ro nếu như bạn không có 1 bản backup thiết bị của bạn.
* Trong nhiều trường hợp, việc sử dụng ứng dụng scan vân tay sẽ dễ dàng hơn. Ứng dụng này hoạt động nhanh hơn và an toàn hơn vì một người bất kỳ không thể copy vân tay của bạn để mở khóa điện thoại của bạn. Nếu bạn muốn tạm thời tắt đi chức năng scan vân tay, hãy tắt thiết bị iOS(iPhone, iPad,...)/Android của bạn và mở/khởi động lại thiết bị. Việc này sẽ bắt bạn nhập mã passcode vào để đăng nhập thiết bị của bạn. Nếu như bạn không có một ứng dụng scan vân tay trên thiết bị Android của bạn, bạn cũng có thể tạo ra một mẫu pattern để mở khóa điện thoại.

![image](https://user-images.githubusercontent.com/526959/47523231-be6e7d80-d8c1-11e8-8332-79b35f245e42.png)

* SIM card của bạn cũng chứa một passcode. Bạn có thể sửa passcode này và đổi nó về một mã 6 chữ số khác trong thiết lập cấu hình điện thoại của bạn, thay vì sử dụng mã mặc định ```0-0-0-0```. Một việc nên làm nữa là hãy chuyển **toàn bộ danh bạ** vào điện thoại của bạn và gỡ chúng khỏi SIM card. Nếu như bạn tình cờ mất điện thoại của mình, thông tin cá nhân các liên lạc của bạn không thể được rút trích ra từ SIM card đó.

### Chỉ cài đặt ứng dụng từ App Store hoặc Google Play
* Hầu hết các điện thoại chứa mã độc bị lây nhiễm qua các ứng dụng không được cài đặt trên các app store chính hãng. Việc này thường xảy ra khi người dùng muốn cài đặt lậu một ứng dụng trả phí hoặc game miễn phí. Ứng dụng "miễn phí" đó có thể chứa mã độc bên trong, được sử dụng để đánh cắp thông tin credit card 💳. Việc này đúng cho cả điện thoại Android lẫn iPhone.
* Hệ điều hành Android còn đặt ra một nguy cơ khác: có rất nhiều ứng dụng trong Google Play Store mà thoạt nhìn có vẻ chính thống, nhưng lại chứa mã độc. Hãy đảm bảo rằng bạn đã **nghiên cứu qua về ứng dụng đó** trước khi tải ứng dụng đó về cài đặt. Hãy tìm kiếm với tên của ứng dụng, đọc các bài review, và kiểm tra số lần mà ứng dụng đó đã được cài đặt cho đến hiện tại. Tóm lại: đừng cài đặt một ứng dụng bất kỳ trên điện thoại hay máy tính bảng Android mà không kiểm tra.
* Một việc quan trọng nữa là hãy kiểm tra các quyền (permission) được yêu cầu bởi ứng dụng. Một ứng dụng chiếu sáng 🔦 chẳng hạn không việc gì cần đến việc truy cập danh bạ điện thoại của bạn. Bạn có thể kiểm tra và chỉnh sửa các quyền được cấp cho ứng dụng trên các hệ điều hành iOS và Android mới nhất. Trên Android, hãy vào ```Settings > Apps```, và trên iOS hãy vào ```Settings > Privacy```.

### Tắt Wifi và Bluetooth khi bạn không cần dùng đến
* Những lực lượng muốn theo dõi bạn có thể **theo dõi bạn** sử dụng WiFi và Bluetooth. Họ có thể theo dõi lộ trình bạn đến trạm xe buýt chẳng hạn. Nếu bạn không cần đến WiFi hay Bluetooth trên đường đi, bạn nên tạm thời tắt các chức năng này đi sử dụng các thiết lập trong mục settings của thiết bị của bạn. Khi ấy bạn đồng thời cũng đã bảo vệ mình trước các kỹ thuật tấn công dành cho WiFi và Bluetooth.
* Nếu như bạn đã từng kết nối đến một mạng WiFi trong quá khứ, thiết bị di động của bạn sẽ tự động kết nối đến mạng đó khi thiết bị của bạn ở gần chúng. Việc này làm phát sinh rủi ro khi mà các hacker thường tạo **các mạng WiFi giả** với các tên trùng với các mạng mà bạn đã từng truy cập đến trước đó, ví dụ như ```Starbucks WiFi``` hay ```McDonald's Free WiFi```. Bởi vì thiết bị di động của bạn nhận ra những mạng này, chúng sẽ cố gắng tự động truy cập đến các mạng này. Đây là một cách để tội phạm mạng cố gắng theo dõi những việc bạn làm trên Internet đồng thời đánh cắp các mật khẩu và thông tin cá nhân của bạn.
* Một hành động khôn ngoan là bạn thường xuyên **xóa danh sách các mạng WiFi được tin tưởng** trên thiết bị di động của bạn. Nếu như bạn kết nối vào một mạng WiFi của một khách sạn 🏨 chẳng hạn, hãy gỡ mạng này khởi bộ nhớ thiết bị của bạn sau khi dùng. Bạn làm việc này bằng cách mở settings trên thiết bị của bạn, lựa chọn mạng WiFi và chọn quên đi (forget) mạng đấy. Bạn cũng nên thiết lập cho thiết bị Android và iOS không tự động kết nối đến từng mạng WiFi riêng lẻ trong phần settings WiFi.

### Tắt chức năng cho phép xem trước thông báo trên màn hình điện thoại được khóa
* Các thông báo có thể chứa các **thông tin nhạy cảm** 🙈, ví dụ như một password mà một người bạn gửi cho bạn qua WhatsApp, hay một mã đăng nhập được gửi đến cho bạn qua tin nhắn điện thoại. Bằng cách ẩn các thông báo này đi trong cửa sổ khóa màn hình ([Android](https://support.google.com/android/answer/9079661), [iOS](https://www.macrumors.com/how-to/hide-text-preview-ios-11/)), sẽ không thấy được nội dung xem trước thông báo (notification) nữa. Chỉ sau khi đã mở khóa (unlock) thiết bị, bạn sẽ có thể thấy được nội dung các thông báo này.

### Sao lưu (backup) các thiết bị của bạn
* Các backup là **vô cùng quan trọng**. Nếu như điện thoại của bạn bị đánh cắp, bạn luôn luôn có thể phục hồi bản backup này lên một điện thoại khác. [Google](https://support.google.com/nexus/answer/2819582) và [Apple](https://support.apple.com/en-us/HT203977) đều có cung cấp các chức năng này để backup hoàn toàn điện thoại của bạn. Đối với nhiều người dùng, các hình ảnh là vật quan trọng nhất đối với họ trên điện thoại. Hãy backup các thiết bị di động của bạn với các dịch vụ như [iCloud](https://www.apple.com/icloud/), [Google Photos](https://photos.google.com/) và [Dropbox](https://db.tt/MOb89WKAbn). Đừng quên kích hoạt xác thực 2 yếu tố (đa nhân tố) cho các dịch vụ này.

## Mạng xã hội và truyền thông

![image](https://user-images.githubusercontent.com/526959/47544665-6744c900-d912-11e8-8ffd-2dedab5f5c60.png)

* Chúng ta chia sẻ một phần lớn cuộc sống của chúng ta qua các mạng truyền thông 🤳. Thỉnh thoảng, việc chia sẻ này là quá nhiều. Đây chẳng khác nào là lời mời gọi công khai cho các hacker thử tấn công bạn. Phương pháp thu thập dữ liệu này còn được gọi là Open Source Intelligence (OSINT), và có thể được sử dụng trong một cuộc tấn công mạng.

### Cẩn thận với thông tin bạn chia sẻ
* Chúng ta thường chia sẻ **các bức ảnh passport, thông tin bằng lái xe và các vé xem ca nhạc** trên các mạng truyền thông. Bạn có thể nghĩ, trời đất, thật là ngu ngốc, và bạn đúng đấy. Dù vậy, việc này vẫn xảy ra rất nhiều 🤦. Barcode trên vé xem ca nhạc của bạn có thể được dùng bởi bất cứ ai, và với một bức ảnh passport của bạn hay bức ảnh bằng lái xe của bạn, người khác có thể vay tiền được với tên của bạn.
* Hãy thận trọng với những gì bạn làm hay chia sẻ trên các mạng truyền thông. Liệu bạn có một người tình cũ vẫn đang theo dõi bạn? Đừng gửi trên các mạng xã hội về việc bạn đã ở đâu trong thời điểm nào. Bạn chia sẻ việc bạn đang chờ một món hàng online ư 📦? Một hacker có thể gọi cho bạn, và hành xử như nhân viên giao hàng của shop online đó, để "kiểm tra thông tin của bạn". Vấn đề quan trọng nhất là bạn cần nhận ra **các nguy cơ/rủi ro đối với bạn là gì**.

### Chú ý thông tin riêng tư
* Nhiều công ty chỉ yêu cầu tên, ngày tháng năm sinh và địa chỉ của bạn để xác thực bạn là người mà bạn cho họ biết. Thông tin này gần như có thể dễ dàng tìm kiếm online. Mọi người thường chúc mừng sinh nhật 🎈 lẫn nhau trên các mạng truyền thông và vô tình cho biết họ sống ở đâu, chỉ bởi đã chia sẻ một bức hình ngôi nhà mới của họ 🏠 lên Instagram chẳng hạn.
* Sử dụng phương pháp này, một hacker nếu lừa/thỏa hiệp được với nhân viên một nhà mạng để đăng ký  số điện thoại người khác với tên của người đó. Việc này cho phép kẻ xấu đó truy cập được các tin nhắn mới trên WhatsApp. Phương pháp hacking này còn được biết với tên gọi **social engineering**; đây là một dạng tấn công mạng có tương tác và điều khiển hành vi con người.
* Những câu trả lời cho **các câu hỏi bí mật** của bạn cũng có thể thường được tìm kiếm online. Nó có thể là tên gọi của con thú cưng đầu tiên của bạn 🐱, hay ngày sinh nhật của mẹ bạn. Hãy chú ý điều này. Sẽ luôn tốt hơn nếu bạn sinh ra **các password ngẫu nhiên** để trả lời cho các câu hỏi bí mật này. Bạn có thể lưu các password là câu trả lời cho các câu hỏi bí mật này trong một ứng dụng quản lý password (password manager).

### Thử tìm kiếm với Google thông tin riêng tư, cá nhân của bạn
* Một hacker sẽ làm gì khi họ muốn thu thập thông tin của đối tượng họ muốn tấn công? Bạn đoán quả không sai: họ sẽ google tên của đối tượng này. Bạn hãy thường xuyên tìm kiếm với Google để biết được thông tin cá nhân mà người khác có thể xem được về bạn. Bạn nên thiết lập [thông báo với Google](https://www.google.com/alerts) để được email mỗi khi tên của bạn xuất hiện kết quả mới với Google. Trong một số trường hợp, thậm chí bạn có thể [gỡ bỏ thông tin này khỏi công cụ tìm kiếm này](https://support.google.com/websearch/troubleshooter/3111061).

![image](https://user-images.githubusercontent.com/526959/47554802-658bfd00-d934-11e8-874b-d3c16b09f9ff.png)

### Thiết lập riêng tư cho các bài viết của bạn và log out tài khoản
* Chúng ta chia sẻ rất nhiều trên các mạng truyền thông. Đó là lý do tại sao chúng ta nên khôn ngoan thiết lập profile của bạn trở nên riêng tư. Bạn có chia sẻ nhiều về cuộc sống đời tư trên Facebook hay Instagram? Nếu có bạn thiết lập Facebook profile của bạn về chế độ riêng tư ([bài viết trong link](https://www.facebook.com/help/288066747875915) sẽ cho bạn biết người khác thấy tài khoản Facebook bạn như thế nào với một người không phải bạn của bạn) và hãy khóa tài khoản Instagram của bạn 🔒, yêu cầu những người dùng phải xin được quyền của bạn cho phép thì mới có thể theo dõi bạn. Lặp lại việc này với tài khoản [Snapchat](https://support.snapchat.com/en-us/a/privacy-settings) của bạn.
* Twitter thì là một câu chuyện khác. Rất nhiều người dùng Twitter để có thể tiếp cận nhiều bạn đọc nhất có thể. Nếu bạn có một Twitter profile, hãy **chú ý đặc biệt đến những gì bạn chia sẻ**, từ vị trí của bạn cho đến các thông tin cá nhân. Và đừng quên log out tài khoản Twitter của bạn, đặc biệt là khi bạn dùng một máy tính công cộng hay laptop của một người bạn.

### Tạo các bản copy điện tử an toàn cho định danh (ID) của bạn
* Bạn hoàn toàn có thể tạo một bản copy điện tử an toàn cho passport, giấy phép lái xe 🚗 hay các giấy tờ chứng minh định danh khác của bạn. Chính quyền Hà Lan đã tạo một ứng dụng giúp bạn thực hiện việc này. Ứng dụng này có tên là [KopieID](https://www.rijksoverheid.nl/onderwerpen/identiteitsfraude/vraag-en-antwoord/veilige-kopie-identiteitsbewijs)(CopyID). Ứng dụng này cho phép bạn che đi các thông tin nhạy cảm như mã số công dân (Citizen Service Number) hay mã số an ninh xã hội (Social Security Number). Bạn có thể thêm một watermark (hình đóng dấu mờ) miêu tả mục đích của bản copy, như là copy để ```ở một khách sạn nào đó vào một ngày nào đó```. Đừng lo lắng: những phần quan trọng nhất của ứng dụng này đều hiển thị bằng tiếng Anh.

### Kiểm tra các thiết bị đã được đăng nhập
* Bạn có ý thức, kiểm soát được tất cả các thiết bị bạn đã từng dùng để truy cập vào các tài khoản của bạn? Và liệu bạn có nhớ log out khi dừng sử dụng các thiết bị đó, như là máy tính bảng của một người bạn hay một máy tính công cộng? Để đảm bảo việc này, hãy kiểm tra danh sách các phiên truy cập vẫn còn hoạt động (active session) mà [Google](https://support.google.com/mail/answer/45938), [Facebook](https://www.facebook.com/help/211990645501187) và [WhatsApp](https://faq.whatsapp.com/en/web/26000018/) cùng nhiều hãng khác cung cấp cho bạn, đồng thời vô hiệu hóa các session mà bạn không nhận biết được.

### Thực hiện kiểm tra bảo mật định kỳ
* Nhiều công ty cung cấp cho bạn lựa chọn kiểm tra các thiết lập bảo mật cho tài khoản của bạn, như [Google](https://myaccount.google.com/security-checkup), [Facebook](https://www.facebook.com/home.php?security_checkup=1) và [Twitter](https://twitter.com/settings/sessions). Bạn có thể thấy được các thiết bị mà tài khoản của bạn đang được đăng nhập vào và các dịch vụ khác có thể truy cập vào thông tin của bạn. Nếu bạn định kỳ kiểm tra các thiết lập bảo mật (security settings) của bạn, bạn sẽ thấy những thiết bị hoặc dịch vụ không còn cần đến quyền truy cập 🛑 vào tài khoản của bạn nữa.

## Nhắn tin và gọi điện thoại

![image](https://user-images.githubusercontent.com/526959/47556238-04febf00-d938-11e8-9915-18156ad3547b.png)

Chúng ta gửi rất nhiều các tin nhắn 💬 và thực hiện các cuộc gọi ☎️ hàng ngày. Vì vậy, chúng ta hãy tìm cách làm cho nó an toàn nhất có thể. Chương này nói về làm sao bạn có thể liên lạc một cách an toàn mà người khác không nghe lén hay đọc trộm các tin nhắn của bạn được.

### Mã hóa đầu cuối ứng dụng
* Việc liên lạc đã trở nên **an toàn hơn nhiều** kể từ tháng 4 năm 2016, khi mà ứng dụng WhatsApp giới thiệu mã hóa đầu cuối ứng dụng. Chức năng này đảm bảo rằng chỉ có thiết bị của người gửi và người nhận có thể đọc được các tin nhắn được gửi bởi họ cho nhau. Nếu một ai đó có thể can thiệp vào để đọc các nội dung tin nhắn được mã hóa đầu cuối ứng dụng, chúng sẽ không khác gì những nội dung vô nghĩa.
* Bạn có thể so sánh với việc gửi một bưu thiếp qua bưu điện. Nếu bạn viết điều gì vào mặt trong của bưu thiếp và dán tem vào bưu thiếp. Với dạng mã hóa thông thường, người đưa thư (trong trường hợp ở đây là ứng dụng WhatsApp) có thể đọc được nội dung bạn gửi trên bưu thiếp. Với những tin nhắn được gửi qua mã hóa ứng dụng đầu cuối, bạn về cơ bản đã đặt bưu thiếp vào một **phong thư được dán lại đặc biệt** ✉️ mà chỉ có người nhận mới có thể đọc được nội dung của bưu thiếp.
* Mã hóa ứng dụng đầu cuối không chỉ được áp dụng cho việc gửi tin nhắn mà còn có thể áp dụng cho việc gửi và nhận các bức ảnh, video, tài liệu và thông tin địa điểm của bạn. Bạn cũng có thể bảo mật các cuộc gọi thoại và video với mã hóa ứng dụng đầu cuối.

### WhatsApp và Facebook
* WhatsApp được sở hữu bởi Facebook; một công ty kiếm ra lợi nhuận bằng cách thu thập nhiều thông tin nhất có thể về người dùng của nó. Bởi vì có mã hóa đầu cuối ứng dụng, Facebook không biết được nội dung các tin nhắn hay các bức ảnh bạn đang gửi. Nhưng Facebook có thể theo dõi được bạn đang liên lạc với những ai. Dạng thông tin này được gọi là **metadata**.

### Những lựa chọn thay thế cho WhatsApp
* Sử dụng ứng dụng chat nào khác là lựa chọn cá nhân của bạn. Một số người chú trọng vào tính dễ sử dụng, trong khi một số người khác chuộng các ứng dụng tập trung vào bảo vệ quyền riêng tư của họ. Có 5 lựa chọn thay thế cho WhatsApp trong tài liệu này.

#### SIGNAL
* [Signal](https://signal.org/) là ứng dụng chat an toàn và hỗ trợ quyền riêng tư nhất. Người dùng có thể cài đặt Signal để các tin nhắn tự động được xóa sau một khoảng thời gian nhất định (từ vài giây cho đến 1 tuần). Signal cũng ít khi lưu thông tin về các người dùng. Dù vậy, ứng dụng Signal có giao diện không phải là rất đẹp và có ít các chức năng hơn các ứng dụng tin nhắn cạnh tranh với nó.

![image](https://user-images.githubusercontent.com/526959/47557283-77709e80-d93a-11e8-9754-d342b69d781d.png)

#### THREEMA
* Ứng dụng chat [Threema](https://threema.ch/en) của Thụy Sĩ là một ứng dụng được ưa thích trong giới nhà báo, bởi vì bạn chỉ phải chia sẻ một username để liên lạc với những người khác. Các phóng viên không phải chia sẻ số điện thoại để sử dụng Threema. Ứng dụng này cũng có một giao diện rất được ưa thích và có nhiều chức năng. Chỉ có 1 nhược điểm duy nhất: bạn cần trả phí 3 USD để cài đặt ứng dụng này. Cũng vì lý do này mà Threema chưa có nhiều người dùng như các ứng dụng miễn phí khác.

![image](https://user-images.githubusercontent.com/526959/47557383-ba327680-d93a-11e8-90ff-712cb4098236.png)

#### WICKR ME
* [Wickr Me](https://wickr.com/) có thể so sánh với Threema: bạn không phải cung cấp một số điện thoại hay địa chỉ email để tạo một tài khoản. Bạn có thể thiết lập các tin nhắn tự động được gỡ bỏ sau một khoảng thời gian cố định, có thể sử dụng ứng dụng này trên nhiều thiết bị và tạo các nhóm. Trái với Threema, Wickr Me miễn phí.

![image](https://user-images.githubusercontent.com/526959/47557318-8f482280-d93a-11e8-9454-c860ff50f094.png)

#### WIRE
* Ứng dụng [Wire](https://wire.com/) của Thụy Sĩ có khá nhiều fan sử dụng trong những năm gần đây, điều này không khiến ta lấy làm lạ bởi các chức năng và thiết kế của Wire. Ứng dụng này sử dụng phương pháp mã hóa của Signal, đồng thời kết hợp một thiết kế đẹp với tính linh hoạt của Telegram. Điều đó có nghĩa là bạn có thể chat từ điện thoại smartphone, trên máy tính hoặc qua trình duyệt web. Các ứng dụng gọi video, **chia sẻ file** hay gửi các ảnh gif đều được bảo vệ với mã hóa đầu cuối ứng dụng.

![image](https://user-images.githubusercontent.com/526959/47557324-98d18a80-d93a-11e8-844c-38800ef4d0da.png)

#### TELEGRAM
* [Telegram](https://telegram.org) không phải là một lựa chọn an toàn, bởi vì ứng dụng này lưu trữ các tin nhắn trên cloud. Một số người thích điều này, bởi vì khi bạn thay đổi điện thoại, bạn có thể bắt đầu chat lại từ điểm bạn đã kết thúc trước đó. Lưu trữ tất cả các tin nhắn, ảnh và video trên cloud đầy những rủi ro. Hãy chú ý điều này khi sử dụng Telegram. Lý do nhiều người sử dụng Telegram là bởi vì nó là một trong những ứng dụng chat thân thiện nhất trên thị trường.

![image](https://user-images.githubusercontent.com/526959/47557356-abe45a80-d93a-11e8-9db3-70e7d38e3e64.png)

#### IMESSAGE
* Ứng dụng chat của Apple chỉ hoạt động trên các thiết bị iPhone và iPad. Các tin nhắn được mã hóa đầu cuối ứng dụng và bạn cũng có thể sử dụng MacBook hay iMac để gửi và nhận các tin nhắn. [iMessage](https://support.apple.com/en-us/HT207006) cũng hỗ trợ nhiều ứng dụng khác, ví dụ như cho phép bạn gọi Uber hay chia sẻ con đường bạn đang đi. Chú ý là Apple lưu giữ metadata của bạn trong vòng 1 tháng.

![image](https://user-images.githubusercontent.com/526959/47557374-b30b6880-d93a-11e8-9da8-84189e469de2.png)

### Tự động xóa tin nhắn
* Các hacker không thể đánh cắp những gì mà bạn không có. Điều này cũng áp dụng với các tin nhắn chat. Nếu như bạn có những cuộc hội thoại nhạy cảm, hãy đảm bảo rằng những tin nhắn đó được tự động xóa 🗑️. [Signal](https://support.signal.org/hc/en-us/articles/360007320771), [Wickr Me](https://support.wickr.com/hc/en-us/articles/115007397548), [Wire](https://support.wire.com/hc/en-us/articles/213216845-How-do-Timed-Messages-work-) và [Telegram](https://telegram.org/faq#q-how-do-self-destructing-messages-work) và nhiều ứng dụng khác đã hỗ trợ chức năng này.

### Gọi thoại và gọi video online
* Bạn có thể sử dụng ứng dụng WhatsApp, Signal và FaceTime bên cạnh một số ứng dụng khác để thực hiện **các cuộc gọi được mã hóa đầu cuối ứng dụng**. Điều đó có nghĩa là dịch vụ bạn sử dụng để gọi điện không thể thấy được hình ảnh của bạn hay nghe được bạn nói gì. Những ứng dụng này được khuyến nghị để thực hiện các cuộc gọi thảo luận các chủ đề nhạy cảm. Nếu bạn muốn dùng ứng dụng [Skype](https://www.skype.com/en/get-skype/) để gọi cho người anh họ ở Úc thì việc thiếu chức năng mã hóa ứng dụng đầu cuối cũng không phải vấn đề lớn.
* Một cuộc gọi với một chiếc điện thoại cũ thông thường 📶 về cơ bản không dễ tấn công với một hacker thông thường nhưng có thể được thực hiện các cuộc tấn công có chủ đích bởi các tổ chức an ninh, tình báo. Chúng ta sẽ bàn thêm về chủ đề này sau.

### Email
* Trái ngược với nhiều ứng dụng chat, email 📨 **hoàn toàn không an toàn**. Trong năm 2018, các nhà cung cấp dịch vụ email đã phối hợp sử dụng thêm các công nghệ khác nhau để vận hành hệ thống email. Việc này khiến chúng không làm cho email an toàn hay ổn định. Chúng ta sử dụng email trong các tình huống kinh doanh (business) và bởi vì nó được chấp nhận rộng rãi, nhưng hãy gửi càng ít thông tin nhạy cảm nhất có thể qua email càng tốt.

## Các chủ đề nâng cao

![image](https://user-images.githubusercontent.com/526959/47564319-d0e2c880-d94e-11e8-9c87-b48b5bc2fbcb.png)

Chúc mừng bạn đã đọc đến đây 👏! Kiến thức của bạn về bảo mật trên không gian mạng (cyber security) đã tăng theo cấp số mũ. Trong chương này, bạn sẽ tìm thấy những thủ thuật cao cấp để làm nản lòng những hacker theo dõi bạn online và dai dẳng.

### Cân nhắc mức độ rủi ro cho cá nhân bạn
* Việc cân nhắc **những nguy cơ, rủi ro bảo mật áp dụng đối với bạn** là rất quan trọng. Bạn là một phụ nữ 👩 đang sử dụng Internet? Vậy là bạn cần bảo vệ bạn khỏi sự quấy rối của những người đàn ông. Bạn là một nhà báo? Khi đó rất có thể là chính quyền sẽ cố gắng theo dõi bạn. Bạn sở hữu một máy tính và một tài khoản ngân hàng?  Bạn thấy đấy: bất kỳ ai cũng có thể là đối tượng của tội phạm mạng, nhưng một số đối tượng đối diện với các nguy cơ cao hơn.
* **Hãy thực hiện những biện pháp thích hợp** tương ứng với mức độ của các nguy cơ, rủi ro dành cho cá nhân bạn. Bài hướng dẫn này cung cấp nhiều lời khuyên, khuyên nghị cho tất cả mọi người thực hiện, bởi vì các mối nguy hiểm có thể đến với bất cứ ai. Nhưng với một nhà hoạt động nữ quyền 💪 với một tài khoản Twitter, sẽ càng quan trọng hơn trong việc giữ địa chỉ nhà bạn và số điện thoại của bạn được ẩn với đám đông.
* Mỗi tình huống đều khác nhau và do đó cần **một cách tiếp cận khác nhau**. Nếu như bạn nghi ngờ tình nhân của bạn đang đọc trộm các email và tin nhắn WhatsApp của bạn, bạn có thể sử dụng chức năng chat của một video game để thông báo cho một người bạn của bạn biết tình trạng của bạn. Khả năng thấp là tình nhân của bạn cũng theo dõi cả những đối thoại đó.

### Nhận diện lừa đảo kĩ thuật số
* Chúng ta bắt đầu với lời khuyên khó nhất, bởi vì nhận diện **lừa đảo kỹ thuật số** được biết là khá nan giải. Lừa đảo kỹ thuật số là dạng lừa đảo mà người cố gắng lừa đảo bạn sẽ gửi bạn một tin nhắn/thông điệp được tạo để đánh lừa bạn theo một dụng ý. Chẳng hạn một hacker có thể thu thập thông tin từ các mạng xã hội mà bạn dùng để tạo một tin nhắn lừa đảo kỹ thuật số có các thông tin khả tín với bạn.
* Giả dụ chuyến bay Delta Airlines ✈️ của bạn đã bị hoãn một giờ và bạn gửi thông tin này lên Facebook. Một hacker có thể sử dụng thông tin này để gửi email cho bạn, cùng thông tin chi tiết một đề nghị bồi thường từ hãng Delta. Tất cả những việc bạn cần làm là đăng nhập một website (mà cung cấp cho hacker password của bạn) và điền vào form đó. Trong khi đó, hacker đang theo dõi những gì bạn gõ vào form website đó.
* Lừa đảo kỹ thuật số thường xảy ra với những người **có rủi ro cao bị tấn công có chủ đích**, như các nhà chính trị, các luật sư và các nhà báo. Tốt nhất là bạn nên cẩn thận cửa nẻo. Nếu như bạn không tin tưởng được việc gì, hãy tìm đến công ty hay tổ chức được giả định là gửi thông điệp cho bạn bằng cách tìm kiếm thông tin công ty đó qua Google, và gọi điện cho họ để hỏi xem liệu thông điệp/tin nhắn mà bạn nhận được có chính thống hay không.

### Mã hóa cho các ổ cứng của bạn và các bản backup
* Bạn có thể mã hóa cho các máy MacBook và iMac của bạn với một click chuột bằng cách kích hoạt chức năng [FileVault](https://support.apple.com/en-us/HT204837). Nó cực kỳ đơn giản và đảm bảo bất cứ ai đánh cắp hay nhặt được laptop của bạn sẽ không thể truy cập vào các file cá nhân của bạn. Đừng đợi chờ nữa: **hãy kích hoạt ngay chức năng này ngay bây giờ**.
* Đối với Windows ta có câu chuyện hoàn toàn khác. Microsoft chỉ cung cấp dịch vụ mã hóa Bitlocker cho các máy tính sử dụng phiên bản Pro của Windows. Tiếc thay phiên bản này lại ít được người dùng cá nhân sử dụng 🤷.
* May mắn là chúng ta có các lựa chọn thay thế để cân nhắc. [VeraCrypt](https://www.veracrypt.fr/en/Downloads.html) là lựa chọn an toàn và đáng tin cậy nhất. Hãy đảm bảo rằng bạn đã backup các file trước khi mã hóa toàn bộ ổ cứng của bạn. Quá trình mã hóa ổ cứng có thể mất hàng giờ đồng hồ và có thể phát sinh vấn đề trong vài trường hợp. Với một bản backup, bạn sẽ đảm bảo được sự an toàn cho các file của bạn.
* Trong cùng chủ đề này: bạn cũng có thể mã hóa các bản backup. Hãy cân nhắc mã hóa ổ cứng gắn ngoài với VeraCrypt chẳng hạn. Một ứng dụng tốt khác là [Cryptomator](https://cryptomator.org), cho phép ngay lập tức mã hóa các file và upload chúng lên cloud. Tuy nhiên, hãy chú ý giữ cẩn thận password của bạn. Mất password của bạn nghĩa là bạn cũng mất đi truy cập đến các file của bạn.

![image](https://user-images.githubusercontent.com/526959/47582330-3dc18700-d97e-11e8-8136-9be83df7b141.png)

### Tạo một password mạnh sử dụng phương pháp Diceware
* Phương pháp Diceware được sử dụng bởi các chuyên gia cho phép tạo ra các password rất mạnh. Diceware sử dụng một lần tung xúc xắc ngẫu nhiên 🎲 và một danh sách dài các từ để sinh các password. Ví dụ [đây](http://world.std.com/~reinhold/dicewarewordlist.pdf) là danh sách các từ tiếng Anh mà bạn có thể sử dụng.
* Bạn bắt đầu bằng cách tung xúc xắc. Thực hiện việc này 5 lần liên tiếp và ghi ra liên tiếp các giá trị nhận được mỗi lần. Bạn sẽ nhận được một số có 5 chữ số và tương ứng với một từ trong danh sách. Ví dụ: nếu bạn tung xúc xắc và nhận được chuỗi ```3-6-4-5-5```, từ mà bạn nhận được tương ứng với chuỗi này là ```limbo```.
* Lặp quá trình này 7 lần để đảm bảo an toàn hoàn toàn. Bạn sẽ nhận được một chuỗi 7 từ tiếng Anh hoàn toàn ngẫu nhiên, ví dụ như ```limbo krebs hoyt ember cometh swipe zaire```. Phương pháp Diceware hiện nay là phương pháp tốt nhất tạo một password mạnh mà bạn có thể nhớ được.

### Xác thực 2 yếu tố (đa nhân tố) với khóa bảo mật (security key)
* Các chuyên gia khuyến nghị sử dụng một khóa vật lý usb còn được gọi là khóa bảo mật (security key) cho xác thực 2 yếu tố (đa nhân tố). Hãy kết nối security key đến các dịch vụ như Google, Facebook, Twtitter và Dropbox và lần tới khi bạn đăng nhập, bạn sẽ được yêu cầu sử dụng khóa bảo mật đó.

![image](https://user-images.githubusercontent.com/526959/47587246-7bc5a780-d98c-11e8-8eb8-89a86684265b.png)

* Gắn khóa usb vào máy tính của bạn và kết nối nó vào điện thoại của bạn để xác thực cho đăng nhập tài khoản của bạn. Dịch vụ online sẽ kiểm tra 👮 khóa usb đó có được gắn với tài khoản của bạn không và khóa bảo mật sẻ giúp bạn chặn việc đăng nhập không đúng ứng dụng hay website ✅. Việc này bảo vệ trước các tấn công lừa đảo kỹ thuật số và các website giả mạo, bởi vì cố gắng đăng nhập chỉ có thể thành công nếu như khóa của bạn và dịch vụ online/website bạn truy cập hợp lệ.
* Bạn được khuyên là nên mua **2 khóa bảo mật** (security key): một để giữ bên người và một làm khóa backup. Hãy kết nối (link) cả 2 khóa usb đến các dịch vụ mà bạn muốn kích hoạt xác thực 2 yếu tố (đa nhân tố). Và đừng quên **tắt đi** những dạng xác thực hai yếu tố khác mà bạn có thể đã kích hoạt cho các dịch vụ này, đặc biệt là gửi mã đăng nhập qua tin nhắn.
* Công ty Thụy Điển Yubico bán các khóa bảo mật này. Lựa chọn thông dụng nhất là [khóa bảo mật màu xanh](https://www.yubico.com/product/security-key-by-yubico/) tương thích với tất cả các dịch vụ online phổ biến. 2 khóa này tốn 36 USD. Khóa bảo mật [Yubikey Neo](https://www.yubico.com/product/yubikey-neo/) hỗ trợ NFC với giá 50 USD, hoạt động được với các thiết bị Android và hỗ trợ tương thích iPhone còn hạn chế. Ngoài ra còn có một phiên bản [USB-c](https://www.yubico.com/product/yubikey-4-series/#yubikey-4c) giá 50 USD.

### Tắt chế độ tự động điền thông tin và kích hoạt chế độ tự động khóa màn hình
* Một số ứng dụng quản lý password cung cấp lựa chọn tự động điền vào các password trên các website cho bạn. Việc này là **không an toàn**. Một hacker có thể đánh lừa ứng dụng quản lý password với một trang giả mạo. Đó là lý do tại sao bạn nên tắt chức năng này, ví dụ là với LastPass.
* Cũng là một lựa chọn thông minh để thiết lập ứng dụng quản lý password tự động khóa chính nó nếu như bạn không sử dụng nó sau một khoảng thời nào đó. Việc này sẽ giữ kho kỹ thuật số (được điền với các password) của bạn không bị phơi bày một cách không cần thiết.

### Thiết bị smartphone như là công cụ theo dõi của hacker và chính quyền
* Các thiết bị smartphone **rất lý tưởng cho việc theo dõi** ai đó. Các cơ quan tình báo 🕵️ thường tác động vào điện thoại của bạn và yêu cầu vị trí của nó, hoặc các hacker có thể thâm nhập vào và kích hoạt microphone và camera mà bạn không hay biết. Hãy chú ý điều này.
* Mặc định Android và iOS theo dõi **vị trí mà bạn đã đi qua** 🔍, và thông tin nhạy cảm này có thể được chia sẻ với các bên thứ ba. Cả [Android](https://support.google.com/accounts/answer/3118687) và [iOS](https://support.apple.com/en-us/HT203033) cho phép bạn tắt đi chức năng này, sau đó điện thoại của bạn sẽ không liên tục lưu lại các vị trí mà bạn đã đi qua. Tuy vậy, việc này vẫn không ngăn được hacker hay cơ quan an ninh, tình báo theo dõi vị trí của bạn sử dụng smartphone của bạn.
* Một biện pháp mạnh hơn là tắt nguồn điện thoại của bạn và giữ nó trong một cái bọc Faraday mà bạn có thể [tự làm](https://killyourphone.com/) hoặc bỏ nó trong một nồi vi sóng (nhưng **đừng bao giờ** bật cho nồi vi sóng này hoạt động nếu như điện thoại của bạn đang ở trong đó). Đây là cách duy nhất để chắc chắn rằng, không ai có thể theo dõi vị trí của bạn.

### Cẩn trọng trong việc backup nội dung chat trên cloud
* Nhiều ứng dụng chat cung cấp lựa chọn lưu nội dung chat trên cloud ☁️, qua Google Drive hoặc iCloud. Hãy cẩn trọng điều này. Tất cả các tin nhắn được mã hóa đầu cuối ứng dụng ngay sau khi đã được gửi đến thiết bị của người nhận thì sẽ mất sự mã hóa này, vì nếu không bạn sẽ không đọc được nội dung của chúng. Nếu bạn lựa chọn backup các tin nhắn của bạn, chúng sẽ được upload lên cloud mà không có mã hóa. Một cơ quan tình báo có thể **yêu cầu lịch sử nội dung chat của bạn**. Hãy chú ý rằng các tin nhắn cũng có thể được backup bởi những người mà bạn chat với họ.

### Thiết lập mật khẩu với các nhà cung cấp dịch vụ cho bạn
* Việc bảo vệ số điện thoại của bạn rất quan trọng, bởi vì nó có thể cung cấp khả năng truy cập đến các mã đăng nhập và mã reset password được gửi đến cho bạn. Các hacker có thể gọi điện đến nhà cung cấp dịch vụ và mạo danh bạn để lấy thông tin nhạy cảm. Trong một số trường hợp, họ thậm chí có thể kiểm soát được số điện thoại của bạn 📱. Hãy yêu cầu nhà cung cấp dịch vụ của bạn để hỏi một password khi phục vụ khách hàng. Nhà cung cấp dịch vụ đó sẽ yêu cầu bạn hay người mạo danh bạn phải cung cấp password trước khi hỗ trợ cho các yêu cầu dịch vụ khách hàng.

![image](https://user-images.githubusercontent.com/526959/47600911-a5191e80-d9f2-11e8-9b9b-7758b0aeb2e4.png)

### Cẩn trọng đối với thông tin vị trí trong các bức ảnh
* Khi bạn sử dụng điện thoại smartphone của bạn để chụp ảnh 🖼️, điện thoại của bạn sẽ lưu giữ tất cả các thông tin đi kèm như ngày, thời gian và địa điểm chụp bức ảnh 🏘️. Thông tin này còn được gọi là EXIF-data. Khi bạn chia sẻ các bức ảnh này lên Facebook, Twitter, Instagram hay WhatsApp, dữ liệu EXIF-data được tự động gỡ bỏ. Tuy nhiên, khi bạn upload một bức ảnh đến website của bạn hay bạn email nó đi, thông tin này vẫn có thể truy cập được bởi những người khác. Nếu bạn muốn đảm bảo rằng EXIF-data được gỡ bỏ, hãy sử dụng website [ImgClean.io](https://imgclean.io/) trước khi upload hay email các bức ảnh của bạn. ImgClean sẽ gỡ khỏi các bức ảnh những thông tin có thêm này và cho bạn tải về một phiên bản sạch của bức ảnh mà bạn có thể chia sẻ một cách an toàn.

### Gọi điện an toàn
* Nếu như bạn muốn gọi cho ai đó mà không có rủi ro **bị nghe lén** 👂, chúng tôi khuyến nghị bạn sử dụng ứng dụng Signal. Signal mã hóa các cuộc gọi với mã hóa ứng dụng đầu cuối. Đối với những người gặp nhiều nguy cơ như các nhà báo và các luật sư, biện pháp này thực sự cần thiết.
* Gọi điện qua Signal (và WhatsApp) cũng bảo vệ bạn trước dạng tấn công **IMSI-catcher**. Những thiết bị này giả làm các cột thu phát sóng điện thoại để nghe lén cuộc gọi và xem trộm tin nhắn của bạn. IMSI-catcher thường được sử dụng bởi các cơ quan an ninh, tình báo nhưng chúng cũng có thể được làm bởi các hacker.

### Email được mã hóa với ProtonMail
* [ProtonMail](https://protonmail.com) là một trong những dịch vụ **thân thiện, dễ dùng** nhất khi ta nhắc đến gửi và nhận các email được mã hóa. Mã hóa đầu cuối ứng dụng chỉ hoạt động khi cả hai người gửi và người nhận đồng thời sử dụng ProtonMail. Với các địa chỉ email khác như Gmail hay Outlook, ProtonMail sẽ hỏi bạn có muốn bảo vệ email với password khi bạn gửi email đi. Người nhận khi ấy sẽ cần password để mở email bạn gửi. ProtonMail làm việc này để thêm một lớp bảo mật bổ sung. Một tài khoản ProtonMail email miễn phí cho bạn dung lượng 500MB, nhưng nếu bạn muốn dung lượng nhiều hơn hay các tính năng bổ sung, bạn sẽ phải trả từ 5 đến 20 USD mỗi tháng.

### Duyệt Internet với Tor
* Ứng dụng [trình duyệt Internet Tor](https://www.torproject.org/) gửi các dữ liệu truy cập mạng của bạn đi xuyên qua nhiều máy tính. Việc này bảo vệ quyền riêng tư của bạn, bởi vì các website không thể tìm ra bạn đến từ đâu và nhà cung cấp dịch vụ mạng không thể thấy được bạn đang làm gì trên Internet. Việc này rất tiện lợi đối với một số người, nhưng nó cũng có thể là một cứu cánh đã cứu mạng nhiều người ở những nước như Iran và Nga. Tor cũng cho phép bạn truy cập các website bị chặn, việc này đặc biệt hữu dụng ở những quốc gia như Thổ Nhĩ Kỳ.

![image](https://user-images.githubusercontent.com/526959/47601856-730eb900-da00-11e8-88f6-87e208c87340.png)

* Tor cũng cho phép truy cập đến **dark web** (thế giới web ngầm) là một phần của Internet mà bạn không thể truy cập với trình duyệt Internet thông thường. Trên dark web, bạn hầu như sẽ thấy các chợ đen bán vũ khí và thuốc phiện, những website chia sẻ phim sex trẻ em hay các cộng đồng cực đoan.
  * Mặt trái của tính ẩn danh mà Tor cung cấp là nó có thể được sử dụng cho các ý định bất chính.
* Hãy biết khi bạn thật sự cần trình duyệt Internet Tor. Bạn có đang tung các thông tin nhạy cảm đến truyền thông báo chí? Nếu vậy thì sử dụng Tor trong một tiệm cafe công cộng có WiFi sẽ giúp tăng tối đa tính ẩn danh của bạn. Tuy nhiên, Internet sẽ chậm hơn nhiều khi sử dụng Tor, vì thế đừng sử dụng Tor sẽ xem các video stream Netflix 📺. Các website cũng có thể nhận biết bạn đang sử dụng Tor để duyệt web và thỉnh thoảng việc này cũng khiến cho các website **chặn các cố gắng đăng nhập tài khoản của bạn**. Do đó, việc sử dụng Tor không được khuyến nghị để thực hiện giao dịch ngân hàng online chẳng hạn.

### Sử dụng PGP (nhưng chỉ khi bạn thật sự phải dùng)
* PGP là chữ viết tắt của **Pretty Good Privacy** là chương trình được sử dụng để mã hóa nội dung và các file đính kèm của các email với mã hóa đầu cuối ứng dụng. Nó đã luôn là một trong những cách tốt nhất để mã hóa các email của bạn trong nhiều năm, nhưng nó cũng rất phức tạp để sử dụng. Hãy nghĩ liệu bạn có thực sự cần PGP 🤔. Sẽ dễ dàng hơn nhiều nếu bạn sử dụng Signal.
* Nếu bạn cần đến PGP nhưng không biết phải thiết lập nó như thế nào, thì bạn nên dùng thử [Keybase](https://keybase.io) trước tiên. Keybase là một mạng xã hội cho phép bạn mã hóa các tin nhắn với PGP khá dễ dàng. Bạn có cần nhiều hơn các chức năng của PGP, như là mã hóa file? Bạn có thể tìm đến một chuyên gia để nhận sự trợ giúp.

### Cài đặt OpenWrt cho thiết bị router của bạn
* Nhiều nhà sản xuất thiết bị ngừng cập nhật các router của họ sau một thời gian xác định. Do đó, chúng tôi khuyến nghị bạn cài đặt [OpenWrt](https://openwrt.org) lên router của bạn. Hệ điều hành này hỗ trợ tất cả các router thường gặp và thường xuyên được cập nhật để vá các lỗ hổng bảo mật 🐛.
* OpenWrt không hoạt động với các modem WiFi được cung cấp và quản lý bởi nhà cung cấp dịch vụ Internet của bạn. Tuy nhiên, bạn có thể mua router của riêng bạn và kết nối nó đến phía sau modem của nhà cung cấp dịch vụ Internet. Thiết lập modem wifi nhà mạng cung cấp cho bạn về trạng thái/chế độ hoạt động ```Bridge/DMZ```, như vậy thiết bị đó chỉ forward (gửi đi) kết nối Internet.

### Chat sử dụng OTR
* **Off The Record (OTR)** là một cách an toàn để chat với mọi người, tương tự Signal. OTR được sử dụng với một địa chỉ email và một ứng dụng máy tính ([Adium](https://adium.im/) cho MacOS và [Pidgin](https://www.pidgin.im/) cho Windows và Linux) hay smartphone ([Conversations](https://play.google.com/store/apps/details?id=eu.siacs.conversations) cho Android và [ChatSecure](https://chatsecure.org/) cho iOS). Những ứng dụng này cho phép bạn chat với những người dùng OTR khác nhưng hầu hết chúng ta sẽ thích ứng dụng Signal hơn.

![image](https://user-images.githubusercontent.com/526959/47602183-2083cb80-da05-11e8-81ca-1691e046b1b8.png)

### Vận hành để sử dụng VPN của riêng bạn
* Nếu bạn rành kỹ thuật, bạn có tự tay vận hành 1 VPN của riêng bạn. Lựa chọn dễ dàng nhất là sử dụng [Algo](https://github.com/trailofbits/algo), cho phép bạn tự cài đặt trên một server mới. Bạn sẽ có thể quản lý kết nối Internet an toàn của bạn và có thể kết nối tất cả các thiết bị của bạn đến nó. Bởi vì Algo rất dễ cấu hình, bạn cũng có thể sử dụng nó để thiết lập một **VPN tạm thời**.

### Tạo một camera giám sát an ninh của riêng bạn
* Người tố giác NSA Edward Snowden đã tham gia làm ứng dụng [Haven](https://guardianproject.github.io/haven/) là một ứng dụng Android miễn phí cho phép biến một smartphone cũ của bạn thành một **camera an ninh thông minh**. Việc này sẽ hữu dụng nếu như bạn nghĩ kẻ xấu có thế tìm cách truy cập vật lý đến các thiết bị của bạn để nhận được các thông tin của bạn, và bằng cách kết nối một thiết bị di động đã bị lây nhiễm mã độc vào laptop của bạn chẳng hạn.
* Haven sử dụng các camera, microphone, các sensor ánh sáng và đo gia tốc của điện thoại smartphone để theo dõi các chuyển động và âm thanh. Đặt chiếc điện thoại smartphone cũ của bạn trong một phòng khách sạn mà bạn đang ở, và bạn sẽ nhận được ảnh báo ngay khi một ai đó vào trong phòng của bạn. Haven cũng chụp các bức ảnh và ghi video của kẻ xâm nhập. Snowden đã từng nhắc đến Haven như một chú chó điện tử canh giữ mà bạn dễ dàng mang theo 🐶.

### iPod Touch và Signal
* Các điện thoại smartphone đang liên tục kết nối đến các trạm phát sóng để nhận các cuộc gọi, tin nhắn và dữ liệu. Việc này để lại nhiều dấu vết metadata, có thể khiến các cơ quan an ninh, tình báo sử dụng được. Những người có nguy cơ cao như các nhà báo, luật sư hay các nhà chính trị cần chú ý điều này. Một thiết bị [iPod Touch](https://www.apple.com/ipod-touch/) với ứng dụng Signal là **lựa chọn an toàn để liên lạc** trong những tình huống như thế. Ứng dụng chơi nhạc của Apple sử dụng hệ điều hành iOS mới nhất có thể truy cập Apple Store và cho phép gọi điện qua wifi đồng thời nhắn tin với Signal. Để tạo một tài khoản Signal, bạn cần một số điện thoại tạm thời. Bạn có thể mua một SIM card trả trước hoặc đăng ký một số VoIP. Thủ thuật này cũng áp dụng cho các iPad (không có chức năng LTE), tuy nhiên các iPad thì quá to để có thể bỏ trong túi quần của bạn dễ dàng.

![image](https://user-images.githubusercontent.com/526959/47602382-55dde880-da08-11e8-96cf-591f13c9779c.png)

### Chú ý các certificate
* Các hacker có thể cố gắng cài đặt các certificate của riêng họ vào máy tính, điện thoại và tablet của bạn, và cho phép họ theo dõi những việc bạn đang làm, ngay cả khi bạn đang vào các website được bảo mật với kết nối HTTPS. Thông thường, nạn nhân trong tình huống này bị lừa cài đặt một certificate lên thiết bị của họ để có thể truy cập một mạng WiFi công cộng. Nhìn chung, **chúng ta không bao giờ nên cài một certificate chỉ để truy cập Internet**, vì vậy hãy đặc biệt cẩn thận khi bạn được yêu cầu cài đặt certificate. Nếu cần thiết, hãy hỏi người quản lý mạng việc yêu cầu cài đặt này có chính thống hay không.

### Sử dụng miếng dán màn hình riêng tư
* Một màn hình riêng tư (privacy screen) là một miếng dán màn hình được đặt lên smartphone, laptop hay máy tính bảng của bạn. Những miếng dán này che đi các góc nhìn, chỉ trừ khi bạn đang nhìn thẳng vào màn hình của bạn, đảm bảo rằng **không ai có thể thấy bạn đang làm việc gì** 👀 từ thiết bị của bạn. Nếu điện thoại của bạn đang được đặt lật ngửa trên bàn, bạn sẽ phải nhấc nó lên và nhìn thẳng vào nó để có thể đọc và thấy các nội dung. [Fellowes](https://www.fellowes.com/us/en/resources/information-security/privacy-screen.aspx) bán những miếng dán bảo vệ tính riêng tư như vậy khá tốt, có giá từ 30 đến 70 USD.

### Sử dụng một lá chắn USB để sạc pin qua cổng USB
* Thiết bị [SyncStop](http://syncstop.com/) đảm bảo khi bạn sạc pin thiết bị của bạn qua cổng USB của một máy tính mà không có dữ liệu nào được sao chép, và **chỉ có điện** được truyền qua. Việc này cản không cho bất cứ mã độc nào được cài đặt lên điện thoại smartphone hay máy tính bảng của bạn. Nếu như bạn muốn sạc pin thiết bị của bạn sử dụng một máy tính không tin tưởng được, SyncStop ngăn chặn các tấn công mã độc cho bạn.

### Tails và Qubes
* Cả hai hệ điều hành này dành cho những người dùng chuyên sâu hoặc đã được huấn luyện, bởi vì hai hệ điều hành này hơi khó vận hành. Cả [Tails](https://tails.boum.org) và [Qubes](https://www.qubes-os.org) được chạy từ thiết bị ổ nhớ di động được kết nối đến máy tính của bạn. Ngừng kết nối các thiết bị USB này khỏi máy tính của bạn và máy tính của bạn sẽ không có dấu vết nào cũng những việc bạn đã làm trước đó. Tails **bảo vệ quyền riêng tư của bạn** và cung cấp tất cả những ứng dụng để làm việc này, ví dụ như Tor, Thunderbird và PGP. Qubes cho bạn **sự bảo vệ tốt nhất** và được sử dụng bởi những người thường bị tấn công bởi các hacker của một chính quyền.
* Hãy nhớ là: nếu bạn thiếu kiến thức kỹ thuật, sử dụng một trong những hệ điều hành này thậm chí có thể làm giảm sự an toàn trên không gian mạng của bạn. Đôi khi sẽ an toàn hơn nếu bạn **cứ sử dụng những thiết bị và dịch vụ mà bạn đã thông thuộc**. Đừng sử dụng một hệ điều hành chỉ vì bạn nghĩ là nó an toàn hơn mà không hiểu rõ về việc sử dụng máy tính an toàn với hệ điều hành đó.

![image](https://user-images.githubusercontent.com/526959/47602645-026d9980-da0c-11e8-9995-29a850ffacb1.png)

## Ghi chú và lời kết.
* Bài hướng dẫn phong phú này được tạo ra nhờ có sự giúp đỡ của 6 chuyên gia (professional hacker): [Maarten van Dantzig](https://twitter.com/maartenvdantzig), [Rik van Duijn](https://twitter.com/rikvduijn), [Melvin Lammerts](https://twitter.com/showthread), [Loran Kloeze](https://twitter.com/lorankloeze), [Sanne Maasakkers](https://twitter.com/sannemaasakkers) và [Sijmen Ruwhof](https://twitter.com/sruwhof). Những minh họa tuyệt vời của bài viết được làm bởi [Laura Kölker](http://laurakolker.nl/). Biên tập viên [Marcel Vroegrijk](https://twitter.com/marcelvroegrijk) đảm bảo mọi nội dung được viết tốt. Phiên bản gốc tiếng Hà Lan của Watch Your Hack được dịch một cách đáng yêu sang tiếng Anh bởi [Kevin Shuttleworth](https://twitter.com/kevwatch) và một lần nữa được biên tập bởi Marcel Vroegrijk.
