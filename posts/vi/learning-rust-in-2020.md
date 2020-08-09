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

Nếu bạn là một Rust beginner, bạn nên bắt đầu với [Exercism's Rust Track](https://exercism.io/tracks/rust). Nếu bạn thấy bế tắc, bạn nên hỏi những người bạn của mình, Google và StackOverflow để nhờ sự giúp đỡ. Tôi khuyến bạn nên dành thời gian để đọc một cách thoải mái và chuyển qua [Rust Standard Library Docs](https://doc.rust-lang.org/std/), một thứ đáng kinh ngạc và có những ví dụ thực tế đơn giản về cách sử dụng mọi thứ bên trong nó. [Rust by Example](https://doc.rust-lang.org/rust-by-example/) cũng là một tài liệu tham khảo thực sự tốt ở mức high-level, thứ mà bạn có thể sử dụng một cách nhanh chóng cho việc học các syntax và tính năng của Rust. Nếu bạn chỉ muốn hiểu sâu hơn về một khái niệm Rust cụ thể nào đó thì tôi thực sự khuyên nên tìm một chương thích hợp trong [The Book](https://doc.rust-lang.org/book/title-page.html) để đọc. Phần tốt nhất trong việc hoàn thành các bài tập trên Exercism là việc bạn có quyền truy cập đến tất cả các solution của các thành viên khác, bạn có thể sắp xếp theo bài có nhiều sao nhất để xem các lời giải rõ ràng và thông minh. Đây là một cách tuyệt vời để học!

Ở thời điểm điểm này, bạn có thể là một advanced beginner và có thể tự tìm con đường của riêng mình. Nếu bạn muốn nhiều hướng dẫn hơn và muốn tiếp tục làm việc trên các chương trình nhỏ và đơn giàn, Tôi khuyên nên làm các bài tập trên [Advent of Code 2018 Calendar](https://adventofcode.com/2018). Lí do tôi khuyên đích danh 2018 calendar là vì một khi bạn hoàn thành một bài tập thì bạn có thể so sánh lời giải của bạn với [BurntSushi's Advent of Code 2018 Rust solutions](https://github.com/BurntSushi/advent-of-code). BurntSushi viết code Rust rất mạch lạc, dễ đọc, và rõ ràng. Đọc code từ một Rustacean có kinh nghiệm sẽ dạy bạn nhiều như chính các bài tập vậy.

Bỏ đọc ngay, phần hay nhất của bài hết rồi.



## Review về các tài nguyên luyện tập Rust

_Alternative title: Reviews of Free Online Resources a Rust Beinnger can use to Practice Writing Small Simple Rust Programs_

Most of these resources weren't specifically created for the purpose of teaching Rust, however they can all be used to learn and practice Rust and many of them explicitly support Rust submissions and provide Rust-specific versions of problems.

The resources are ordered from worst to best.



### [HackerRank](https://www.hackerrank.com)

Rust is a supported language on HackerRank except you aren't allowed to submit Rust solutions to most of the problems on their site. I tried to upload my solution directly and they refused it:

![hackerrank more like failrank](../assets/hackerrank-more-like-failrank.png)

This is really strange because I was able to browse Rust solutions for the problem above submitted by other HackerRank users, so it's possible to submit a Rust solution somehow. I tried Googling this issue and but Google didn't return any useful results. There's no way for me to evalute HackerRank other than to tell you not to waste your time with it like I did.



### [Project Euler](https://projecteuler.net/archives)

When I first started to learn programming back in 2012 I commonly heard _"If you wanna get up to speed quickly in a new programming language solve some Project Euler problems with it!"_ which was okay advice at the time since there were not many other alternatives but in my opinion Project Euler has very little to do with programming. Project Euler problems are more math problems than they are programming problems. Their challenge lies almost entirely in the mathematical reasoning required to reach the solution as the programming required is usually trivial. I would not recommend solving Project Euler problems as a way to learn Rust unless you're very mathematically inclined and have some nostalgia for the site.



### [LeetCode](https://leetcode.com/problemset/all/)

Rust is a supported language on LeetCode. For every problem on LeetCode you get a solution template which usually contains a single unimplemented function which you then have to implement and submit in order to solve the problem. For more involved problems the solution template might include a `struct` and an `impl` block with several unimplemented methods. Unfortunately, these solution templates are not created by humans, they are automatically generated, which results in a lot of really awkward and unidiomatic Rust code. Examples:

| LeetCode generated Rust | Idiomatic Rust |
|-|-|
| tree problems represent links as `Option<Rc<RefCell<Node>>>` | `Option<Rc<RefCell<Node>>>` is overkill for tree links and `Option<Box<Node>>` works just as well and is much easier to work with |
| methods which obviously mutate self still borrow it immutably, e.g. `fn insert(&self, val: i32)` | methods that mutate self need to borrow it mutably, e.g. `fn insert(&mut self, val: i32)` |
| signed 32-bit integers are used for all numbers, even if the problem is undefined for nonnegative integers, e.g. `fn nth_fib(n: i32) -> i32` | problems which are undefined for nonnegative integers should use unsigned integers, e.g. `fn nth_fib(n: u32) -> u32` |
| functions always take ownership of their arguments, even if it's unnecessary, e.g. `fn sum(nums: Vec<i32>) -> i32` | if you don't need ownership then borrow `fn sum(nums: &[i32]) -> i32` |
| functions sometimes ignore basic error cases, e.g. for `fn get_max(nums: Vec<i32>) -> i32` what `i32` should be returned if `nums` is empty? | if a result might be undefined the return type should be wrapped in an `Option`, e.g. `fn get_max(nums: &[i32]) -> Option<i32>` |

Other LeetCode issues, specific to Rust:
- LeetCode doesn't allow you to pull in 3rd-party dependencies in solutions. Normally I think this is okay for most languages but Rust in particular has a pretty slim standard library which doesn't even include regex support so a lot of the more complex string parsing problems on LeetCode are pointlessly difficult to solve in Rust but have otherwise trivial solutions in other languages which have regex support in their standard libraries.
- None of the problems in the `concurrency` category accept solutions in Rust. What? Fearless concurrency is one of Rust's major selling points!
- After solving a problem you can go to the problem's comments section to see other user's solutions (as many users like to publish their solutions there) but because Rust isn't very popular on LeetCode sometimes you won't find any Rust solutions ;(

General LeetCode issues:
- LeetCode has a surprising amount of very low quality problems. Problems can be liked and disliked by users but problems are never removed even if they hit very high dislike ratios. I've seen lots of problems with 100+ votes and 80%+ dislike ratios and I don't understand why they are kept on the site.
- Problem difficulty ratings are kinda off. Problems are rated as Easy, Medium, or Hard but there are many Easy problems with lower solve rates than many Hard problems.
- Not all problems accept solutions in all languages, and you can't filter problems by which languages they accept. None of the graph problems on LeetCode accept Rust solutions, for example.
- LeetCode blocks "premium" problems behind a steep monthly paywall but doesn't offer any kind of premium free-trial so there's no telling if the quality is actually any better than the free problems.

Things LeetCode does right:
- Solutions to problems are tested against a suite of secret unit tests, but if you fail a particular test case they show you the failed case.
- All of the generated Rust code at least follows rustfmt conventions.



### [Codewars](https://www.codewars.com/join?language=rust)

Codewars is a misleading name. There's no war going on at Codewars. There's no time limit to solve problems and your solutions aren't judged on their speed of execution or memory useage. You aren't in competition with anyone else. This isn't a bad thing, just worth pointing out.

Rust is a supported language on Codewars. For every problem on Codewars you get a solution template which usually contains a single unimplemented function which you then have to implement and submit in order to solve the problem. These solution templates are created by humans, including humans who aren't familiar with Rust, so you occasionally get some awkward and unidiomatic Rust. Examples:

| Codewars' Rust Problems | Idiomatic Rust |
|-|-|
| sometimes don't follow rustfmt conventions, e.g. `fn makeUppercase(s:&str)->String` | always follows rustfmt conventions, e.g. `fn make_uppercase(s: &str) -> String` |
| sometimes takes signed integer arguments for problems that aren't defined for nonnegative integers, e.g. `fn nth_fib(n: i32) -> i32` | if a problem isn't defined for nonnegative integers use unsigned integer arguments, e.g. `fn nth_fib(n: u32) -> u32` |
| sometimes a problem asks you to return `-1` for the null case, e.g. `fn get_index(needle: i32, haystack: &[i32]) -> i32` | if a result can be null the return type should be wrapped in an `Option`, e.g. `fn get_index(needle: i32, haystack: &[i32]) -> Option<usize>` |
| sometimes don't take advantage of deref coercion, e.g. `fn do_stuff(s: &String, list: &Vec<i32>)` | takes advantage of deref coercion, e.g. `fn do_stuff(s: &str, list: &[i32])` |

All of the issues above only happen sometimes since there are Rustaceans of various skill-levels on Codewars translating problems to Rust. This is a huge step up from LeetCode where all of the generated Rust problem code is consistently unidiomatic. However, the Rust community on Codewars as a whole might lean towards the inexperienced side since I've seen some highly upvoted "idiomatic" solutions that were also a bit on the awkward side. Examples:

| Codewars' highest upvoted Rust solutions | Idiomatic Rust |
|-|-|
| sometimes use an explicit return at the end of a function block, e.g. `return result;` | blocks are evaluated as expressions and implicitly return their last item, an explicit return at the end of a function block is unnecessary, e.g. `result` |
| often use compact formatting to make the solution look more concise | should follow rustfmt conventions |
| sometimes make unnecessary allocations, e.g. `str_slice.to_string().chars()` | if you don't need to allocate then don't, e.g. `str_slice.chars()` |
| often try to solve the problem using nothing but iterators at the cost of everything else | iterators are expressive and idiomatic, but if you have to chain 15 of them in a row and there are multiple levels of nested iterators in-between then perhaps you should consider refactoring to use some helper functions, intermediate variables, and maybe even a for-loop |

Again, the issues above only happen sometimes. An experienced Rustacean can spot them easily but there are a lot of Rust newbies on these sites who have no clue they are learning anti-patterns.

Other Codewars issues, specific to Rust:
- Rust doesn't seem that popular on Codewars, the site has 9000 exercises but only 300 of them have been translated to Rust ;(

Other general Codewars issues:
- Your solution is tested against a suite of secret unit tests, if you fail one of the secret unit tests you aren't shown the failed test case. This is especially annoying if the test case tests for an edge case that wasn't clearly communicated in the problem description.

Things Codewars does right:
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
