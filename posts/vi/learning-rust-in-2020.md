# Học Rust vào năm 2020

_Ngày 9 tháng 5, 2020 · 15 phút đọc · #rust_

**Mục lục**
- [Giới thiệu](#giới-thiệu)
- [TL;DR](#tldr)
- [Review về các tài nguyên luyện tập Rust](#review-về-các-tài-nguyên-luyện-tập-rust)
    - [HackerRank](#hackerrank)
    - [Project Euler](#project-euler)
    - [LeetCode](#leetcode)
    - [Codewars](#codewars)
    - [Advent of Code](#advent-of-code)
    - [Rustlings](#rustlings)
    - [Exercism](#xxercism)
- [Kết luận](#kết-luận)
- [Bàn luận](#bàn-luận)
- [Các thông báo](#các-thông-báo)
- [Đọc thêm](#đọc-thêm)



## Giới thiệu

Khi tôi bắt đầu học Rust, tôi đã mắc phải sai lầm khi làm theo lời khuyên đọc [Cuốn sách này](https://doc.rust-lang.org/book/title-page.html) trước tiên. Mặc dù đó là một tài nguyên tuyệt vời, nó lại hơi quá sức đối với một người mới bắt đầu khi được bảo rằng _"Nếu bạn muốn học ngôn ngữ lập trình này, cách tốt nhất để bắt đầu là hãy đọc 20 chương sách này!"_ Hầu hết mọi người đều bỏ cuộc trước cả khi bắt đầu nếu nghe được những lời khuyên như thế. Không ai lại đi nói rằng cần đọc 20 chương sách chỉ để bắt đầu với Javascript hoặc Python cả. Learning curve của Rust thực sự không phải là chuyện đùa nhưng bạn nên đưa cho mọi người thứ họ muốn, và họ muốn lập trình, không phải đọc về lập trình. Lập trình thì vui vẻ nhưng đọc về lập trình thì không vui đến thế.

10% đầu tiên của bài này là để tôi đưa ra lời khuyên cho bạn làm thế nào để học Rust vào năm 2020 theo hướng tiếp cận _trăm thấy không bằng một lần thử (practical hands-on coding)_. Đây là một phần hay của bài viết. Bạn có thể không cần đọc tiếp phần còn lại sau phần này (Tôi sẽ nói với bạn là khi nào). 90% còn lại của bài viết này là để tôi "ca ngợi" phần lớn các trang làm về coding challenge hỗ trợ Rust nghèo nàn đến mức nào.



## TL;DR

Nếu bạn là một người mới hoàn toàn với Rust và muốn học nhiều nhất có thể chỉ trong một ngày thì nên đọc một bài viết xuất sắc, [A half-hour to learn Rust](https://fasterthanli.me/blog/2020/a-half-hour-to-learn-rust/) của fasterthanlime và sau đó ngó qua repo [Rustlings](https://github.com/rust-lang/rustlings) tuyệt vời này và hoàn thành các bài tập.

Nếu bạn là một Rust beginner, bạn nên bắt đầu với [Exercism's Rust Track](https://exercism.io/tracks/rust). Nếu bạn thấy bế tắc, bạn nên hỏi những người bạn của mình, Google và StackOverflow để nhờ sự giúp đỡ. Tôi khuyên bạn nên dành thời gian để đọc một cách thoải mái và chuyển qua [Rust Standard Library Docs](https://doc.rust-lang.org/std/), một thứ đáng kinh ngạc và có những ví dụ thực tế đơn giản về cách sử dụng mọi thứ bên trong nó. [Rust by Example](https://doc.rust-lang.org/rust-by-example/) cũng là một tài liệu tham khảo thực sự tốt ở mức high-level, thứ mà bạn có thể sử dụng một cách nhanh chóng cho việc học các syntax và tính năng của Rust. Nếu bạn chỉ muốn hiểu sâu hơn về một khái niệm Rust cụ thể nào đó thì tôi thực sự khuyên nên tìm một chương thích hợp trong [The Book](https://doc.rust-lang.org/book/title-page.html) để đọc. Phần tốt nhất trong việc hoàn thành các bài tập trên Exercism là việc bạn có quyền truy cập đến tất cả các solution của các thành viên khác, bạn có thể sắp xếp theo bài có nhiều sao nhất để xem các lời giải rõ ràng và thông minh. Đây là một cách tuyệt vời để học!

Ở thời điểm điểm này, bạn có thể là một advanced beginner và có thể tự tìm con đường của riêng mình. Nếu bạn muốn nhiều hướng dẫn hơn và muốn tiếp tục làm việc trên các chương trình nhỏ và đơn giản, Tôi khuyên nên làm các bài tập trên [Advent of Code 2018 Calendar](https://adventofcode.com/2018). Lí do tôi khuyên đích danh 2018 calendar là vì một khi bạn hoàn thành một bài tập thì bạn có thể so sánh lời giải của bạn với [BurntSushi's Advent of Code 2018 Rust solutions](https://github.com/BurntSushi/advent-of-code). BurntSushi viết code Rust rất mạch lạc, dễ đọc, và rõ ràng. Đọc code từ một Rustacean có kinh nghiệm sẽ dạy bạn nhiều như chính các bài tập vậy.

Bỏ đọc tiếp thôi, phần hay nhất của bài đã hết rồi.



## Review về các tài nguyên luyện tập Rust

_Tiêu đề thay thế: các review về các tài nguyên online miễn phí mà một Rust beginner có thể dùng để luyện tập viết các chương trình Rust nhỏ và đơn giản_

Hầu hết các tài nguyên này đều không được tạo ra với mục đích dạy Rust, nhưng dù sao chúng vẫn có thể được dùng để học và luyện tập Rust. Rất nhiều trong số chúng hỗ trợ các Rust submission một cách rõ ràng và cung cấp các phiên bản dành riêng cho Rust của các vấn đề đó.

Những tài nguyên này được sắp xếp theo thứ tự từ tệ nhất đến tốt nhất.



### [HackerRank](https://www.hackerrank.com)

Rust là một ngôn ngữ được hỗ trợ trên HackerRank ngoài việc bạn không được phép submit các lời giải bằng Rust lên hầu hết các problem ở trên trang của họ. Tôi đã cố để upload lời giải bằng Rust của mình một cách trực tiếp nhưng họ đã từ chối nó:

![hackerrank more like failrank](../../assets/hackerrank-more-like-failrank.png)

Nó thật sự lạ bởi vì tôi có thể thấy các lời giải bằng Rust cho problem trên của các người dùng khác trên HackerRank, vì vậy sẽ là khả thi cho việc submit một lời giải bằng Rust theo một cách nào đó. Tôi đã thử Google vấn đề này nhưng Google không trả về một kết quả có ích nào. Không có cách nào cho tôi để đánh giá HackerRank ngoài việc nói với bạn rằng đừng lãng phí thời gian với nó giống như tôi đã làm.



### [Project Euler](https://projecteuler.net/archives)

Khi tôi bắt đầu học lập trình lần đầu tiên vào năm 2012, tôi thường được nghe _"Nếu bạn muốn tăng tốc nhanh chóng trong việc học một ngôn ngữ mới thì hãy đi giải một vài Project Euler problem bằng nó"_ và đó là một lời khuyên ổn ở thời điểm khi không có quá nhiều lựa chọn thay thế. Nhưng theo quan điểm của tôi thì Project Euler có quá ít thứ để làm với lập trình. Các problem trên Project Euler giống các problem về toán hơn là các problem về lập trình. Gần như toàn bộ challenge của họ yêu cầu người làm phải có lý luận toàn học hơn là kỹ năng lập trình. Tôi không khuyến khích giải quyết các problem trên Project Euler như là một cách để học Rust trừ khi bạn là một người rất thiên về toán và có chút hoài niệm với trang này.



### [LeetCode](https://leetcode.com/problemset/all/)

Rust là một ngôn ngữ được hỗ trợ trên LeetCode. Hầu hết các problem trên LeetCode đều có các template sẵn cho lời giải bao gồm một hàm chưa được cài đặt, nơi mà sau đó bạn sẽ code và submit để giải quyết problem. Trong hầu hết các problem, các template này sẽ bao gôm một `struct` và một block `impl` với một vài hàm chưa được cài đặt. Không may là, các template này không được tạo ra một cách thủ công, chúng được tạo ra một các tự động và hậu quả là có rất nhiều code Rust thực sự khó hiểu và đơn lẻ. Ví dụ:

| Rust được sinh bởi LeetCode | Rust chuẩn |
|-|-|
| các problem về cây biểu diễn node bằng `Option<Rc<RefCell<Node>>>` | `Option<Rc<RefCell<Node>>>` có vẻ hơi bị dao mổ trâu với node và `Option<Box<Node>>` có thể hoạt động tốt như thế mà dễ sử dụng hơn nhiều |
| methods which obviously mutate self still borrow it immutably, e.g. `fn insert(&self, val: i32)` | methods that mutate self need to borrow it mutably, e.g. `fn insert(&mut self, val: i32)` |
| signed 32-bit integers are used for all numbers, even if the problem is undefined for nonnegative integers, e.g. `fn nth_fib(n: i32) -> i32` | problems which are undefined for nonnegative integers should use unsigned integers, e.g. `fn nth_fib(n: u32) -> u32` |
| functions always take ownership of their arguments, even if it's unnecessary, e.g. `fn sum(nums: Vec<i32>) -> i32` | if you don't need ownership then borrow `fn sum(nums: &[i32]) -> i32` |
| functions sometimes ignore basic error cases, e.g. for `fn get_max(nums: Vec<i32>) -> i32` what `i32` should be returned if `nums` is empty? | if a result might be undefined the return type should be wrapped in an `Option`, e.g. `fn get_max(nums: &[i32]) -> Option<i32>` |

Các vấn đề khác trên LeetCode, dành riêng cho Rust:
- LeetCode không cho phép bạn dùng thư việc bên thứ 3 để giải quyết vấn đề. Thông thường thì tôi nghĩ là nó ổn đối với hầu hết các ngôn ngữ nhưng riêng Rust thì  lại có thư viện chuẩn tương đối đơn giản, đến nỗi không support cả biểu thức chính quy cho nên có rất nhiều vấn đề khi parse các chuỗi string phức tạp trên LeetCode bằng Rust. Trong khi việc đó chả đáng là gì đối với các ngôn ngữ có hỗ trợ sẵn biểu thức chính quy trong thư viện chuẩn của chúng.
- Không một problem nào trong mục `concurrency` chập nhận các lời giải bằng Rust. Cái gì? `Fearless concurrency` là một trong những tính năng cực kì đắt giá của Rust!
- Sau khi giải quyết xong prolem, bạn có thể đến phần comment của problem để xem lời giải của những ngừoi khác (bởi vì rất nhiều người thích để lời giải của họ ở đó) nhưng đen ở chỗ là Rust không được phổ biến lắm trên LeetCode nên thỉnh thoảng sẽ không thấy lời giải bằng Rust nào ;(

Các vấn đề chung trên LeetCode:
- LeetCode có một lượng đáng kinh ngạc các problem có chất lượng vô cùng thấp. Các problem được like và dislike bởi người dùng nhưng lại không bao giờ được xoá đi mặc dù chúng có một tỉ lệ dislike rất cao. Tôi từng thấy nhiều problem có hơn 100 vote mà trong đó hơn 80% là dislike. Tôi thắc mắc là tại sao chúng vẫn được giữ ở đó
- Xếp hạng độ khó của problem hình như có vấn đề. Các problem được xếp  hạng là Dễ, Trung bình, hoặc Khó nhưng có rất nhiều problem Dễ lại có tỉ lệ giải thấp hơn rất nhiều so với các problem Khó.
- Không phải tất cả các problem đều hỗ trợ tất cả các ngôn ngữ. Và bạn không thể lọc các problem theo ngôn ngữ mà chúng support. Ví dụ là không có một problem nào vễ graph trên LeetCode chấp nhận lời giải Rust cả.
- LeetCode chặn các problem "premium" sau một bức tường phí hàng tháng siêu to khổng lồ mà lại không cho phép dùng thử. Vì vậy chả có gì đảm bảo là các problem cao cấp này lại tốt hơn các problem miễn phí cả.

Các thư mà LeetCode đã làm đúng:
- Các lời giải được kiểm tra bằng các unit test bí mật, nhưng nếu bạn fail một test case cụ thể nào đó thì họ sẽ chỉ ra cho bạn.
- Tất cả các code Rust được sinh tự động ít nhất là đã tuân theo các convention của rustfmt.



### [Codewars](https://www.codewars.com/join?language=rust)

Codewars là một cái tên gây hiểu nhầm. Không có cuộc thi nào đang diễn ra ở Codewars cả. Không có giới hạn thời gian để giải quyết vấn đề và các lời giải của bạn cũng không được đánh giá dựa trên thời gian cũng như bộ nhớ đã sử dụng. Bạn không phải ganh đua với những người khác. Đây không phải là một điều tệ, chỉ là đáng để chỉ ra thôi.

Rust được hỗ trợ trên Codewars. Với mỗi problem trên Codewars, bạn có một template cho lời giải thường bao gồm một hàm chưa được viết, là nơi bạn sẽ cài đặt hàm và sau đó submit lên. Các template này được tạo thủ công bằng sức người, bao gồm cả những người không quen với Rust nữa, vì vậy thỉnh thoảng bạn vẫn sẽ thấy một số code Rust trông có vẻ kỳ cục và không đúng chuẩn lắm. Ví dụ:

| Các vấn đề về Rust của Codewars | Rust chuẩn |
|-|-|
| sometimes don't follow rustfmt conventions, e.g. `fn makeUppercase(s:&str)->String` | always follows rustfmt conventions, e.g. `fn make_uppercase(s: &str) -> String` |
| sometimes takes signed integer arguments for problems that aren't defined for nonnegative integers, e.g. `fn nth_fib(n: i32) -> i32` | if a problem isn't defined for nonnegative integers use unsigned integer arguments, e.g. `fn nth_fib(n: u32) -> u32` |
| sometimes a problem asks you to return `-1` for the null case, e.g. `fn get_index(needle: i32, haystack: &[i32]) -> i32` | if a result can be null the return type should be wrapped in an `Option`, e.g. `fn get_index(needle: i32, haystack: &[i32]) -> Option<usize>` |
| sometimes don't take advantage of deref coercion, e.g. `fn do_stuff(s: &String, list: &Vec<i32>)` | takes advantage of deref coercion, e.g. `fn do_stuff(s: &str, list: &[i32])` |

Tất cả các vấn đề trên chỉ thỉnh thoảng xảy ra bởi vì có các Rustaceans ở rất nhiều trình độ trên Codewars chuyển các problem của họ sang Rust. Đây là một bước tiến lớn so với LeetCode, nơi tất cả code Rust sinh ra bị không đúng chuẩn và đồng nhất. Mặc dù vậy, cộng đồng Rust trên Codewars có vẻ phần lớn là thiếu kinh nghiệm bởi vì tôi đã từng thấy một vài lời giải có số vote nhiều lại có code hơi kỳ cục chút. Ví dụ:

| Codewars' highest upvoted Rust solutions | Idiomatic Rust |
|-|-|
| sometimes use an explicit return at the end of a function block, e.g. `return result;` | blocks are evaluated as expressions and implicitly return their last item, an explicit return at the end of a function block is unnecessary, e.g. `result` |
| often use compact formatting to make the solution look more concise | should follow rustfmt conventions |
| sometimes make unnecessary allocations, e.g. `str_slice.to_string().chars()` | if you don't need to allocate then don't, e.g. `str_slice.chars()` |
| often try to solve the problem using nothing but iterators at the cost of everything else | iterators are expressive and idiomatic, but if you have to chain 15 of them in a row and there are multiple levels of nested iterators in-between then perhaps you should consider refactoring to use some helper functions, intermediate variables, and maybe even a for-loop |

Một lần nữa, các vấn đề trên chỉ thỉnh thoảng xảy ra. Một Rustacean có kinh nghiệm có thể dễ dàng phát hiện ra nhưng có rất nhiều Rust newbie trên những trang này không thể nhận ra rằng họ đang học các anti-pattern.

Các vấn đề khác của Codewars, cụ thể là với Rust:
- Rust có vẻ không được phổ biến lắm trên Codewars, trang này có 9000 bài tập nhưng chỉ có 300 trong số đó là được chuyển sang Rust ;(

Các vấn đề chung khác của Codewars:
- Lời giải của bạn được kiểm tra bằng các unit test bí mật, nếu bạn fail ở một test case thì nó sẽ không được chỉ ra cho bạn. Nó thật sự khó chịu nếu test case này kiểm tra một trường hợp ở biên, mà trường hợp này không được giải thích rõ trong mô tả của problem.

Các thứ Codewars làm đúng:
- There's a small whitelist of 3rd-party dependencies you can use to help solve problems with Rust. This whitelist includes: rand, chrono, regex, serde, itertools, and lazy_static which helps round out Rust's standard library and puts it more on par with other languages.
- You can filter problems by language.
- Submitting a solution to a problem also automatically publishes the solution. You can view and upvote other members' solutions. You can sort solutions by most upvotes to see particularly concise and clever solutions, which sometimes will also be very idiomatic (but sometimes not, as explained above).
- Problem difficulty grading is pretty good! Instead of grading problems as Easy, Medium, or Hard like LeetCode, Codewars chooses to grade problems from easiest to hardest as: 8 kyu, 7 kyu, 6 kyu, 5 kyu, 4 kyu, 3 kyu, 2 kyu, 1 kyu. I completed 60 problems in the 8 kyu - 4 kyu range and every level felt a little more difficult than the last, which aligned with my expectations.



### [Advent of Code](https://adventofcode.com/)

Advent of Code is totally language-agnostic. This would seem like a minus at first but seeing how horribly HackerRank, LeetCode, and Codewars handle their support for Rust on their sites it's actually a plus. Advent of Code also gets placed above the previously mentioned sites because AoC's exercises are really interesting, diverse, and high quality in my opinion.

General AoC issues:
- After you finish an exercise there's no way to see other people's Rust solutions unless you search from them on Google, and even after you find some there's no telling how good or idiomatic they are.

To solve the above issue I recommend going through the 2018 Calendar problems and comparing your solutions to [BurntSushi's AoC 2018 Rust solutions](https://github.com/BurntSushi/advent-of-code). BurntSushi writes really clean, readable, idiomatic Rust code. If you want to go through the 2019 Calendar then I recommend comparing your solutions to [bcmyers' AoC 2019 Rust solutions](https://github.com/bcmyers/aoc2019). The reason I specifically suggest bcmyers' is because he made a [youtube playlist of him coding up the solutions](https://www.youtube.com/playlist?list=PLQXBtq4j4Ozkx3r4eoMstdkkOG98qpBfg) and he does a great job of explaining his thought process and why he's doing what he's doing while he's coding.

Things AoC got right:
- High quality, interesting, curated exercises that are tied together with a narrative.
- Language agnostic, so while it doesn't teach you any Rust patterns it at least doesn't teach you any Rust anti-patterns either.



### [Rustlings](https://github.com/rust-lang/rustlings)

Rustlings is sooo good. All Rustlings exercises are hand-crafted for Rust with love and it's a wonderful breath of fresh air. Finally, a set of exercises that really teach you idiomatic Rust!

If you're a total Rust newbie you should absolutely checkout [Rustlings](https://github.com/rust-lang/rustlings) and get started on the exercises. I highly recommend reading fasterthanlime's [A half-hour to learn Rust](https://fasterthanli.me/blog/2020/a-half-hour-to-learn-rust/) first as it'll get you up to speed on a lot of Rust syntax and concepts super quickly.

I have only 1 tiny Rustlings criticism: there are some sudden difficulty spikes in the "error-handling" and "conversions" exercises that I could see some users getting overwhelmed by. I assume most probably make it through, or at least I hope.

I also have 1 tiny non-criticism: it's too short. This is a non-criticism because it's one of Rustlings design goals to be a quick and gentle introduction to Rust but it's so good that of course I wish it was somehow longer.



### [Exercism](https://exercism.io/tracks/rust)

Exercism has a Rust track, which is a collection of exercises roughly ordered by subject and difficulty. The Rust track shares a lot of exercises in common with other tracks, but all of the exercises were translated to Rust by experienced Rustaceans and don't suffer from any of the awkward unidiomatic Rust issues that are common on LeetCode and Codewars. There are about a dozen Rust-specific problems that require you to implement a standard library trait, or write a macro, or write a parallel solution using multiple threads, or write unsafe Rust code. These exercises are by far the highlights of the track and I wish there were more of them. Exercism is second only to Rustlings as a resource for learning Rust. The only reason I placed it above Rustlings is Rustlings can be completed in an evening and Exercism's Rust track will take at least a month to complete so it just has a lot more content.

Exercism issues, specific to the Rust track:
- "Mentored mode" is useless, as most of the Rust mentors on the site are inactive, and the students heavily outnumber them, so it's much better to go through a track in "practice mode".
- There are 92 exercises but a good chunk of them don't really teach you anything new so they kinda feel like busywork. They could probably cut ~20 exercises from the track to make it feel a lot tighter.

Things Exercism does right:
- All problems are translated to Rust or written for Rust by experienced Rustaceans.
- There are problems which specifically teach Rust's idioms, design patterns, and unique features.
- Problem difficulties are fairly graded, easy problems are easy, medium problems are medium, hard problems are hard.
- You can include whatever 3rd-party dependencies that you want in your solutions.
- All unit tests are public, if you're failing a test you know exactly why.
- After you submit a solution you can browse other user's solutions, and you can sort solutions by which received the most stars.



## Kết luận

Giống như [TL;DR](#tldr) thôi :)



## Bàn luận

Bàn luận về bài này trên
- [learnrust subreddit](https://www.reddit.com/r/learnrust/comments/ggj8tf/learning_rust_in_2020/)
- [official Rust users forum](https://users.rust-lang.org/t/blog-post-learning-rust-in-2020/42373)
- [Twitter](https://twitter.com/pretzelhammer/status/1259897499122360322)
- [rust subreddit](https://www.reddit.com/r/rust/comments/gie64f/learning_rust_in_2020/)
- [Hackernews](https://news.ycombinator.com/item?id=23160975)



## Các thông báo

Nhận thông báo khi một bài đăng được xuất bản bằng cách
- [Theo dõi pretzelhammer trên Twitter](https://twitter.com/pretzelhammer) hoặc
- Watching các bản release của repo này (nhấn vào `Watch` dropdown và chọn `Releases only`)



## Đọc thêm

- [Common Rust Lifetime Misconceptions](./common-rust-lifetime-misconceptions.md)
- [Sizedness in Rust](./sizedness-in-rust.md)
