# 8주차 JAVA 중간고사 실기시험

For this test, you will create a LibrarySystem class that utilizes a LibraryBook class which is based on a Book interface.
이 시험에서는 Book 인터페이스를 기반으로 하는 LibraryBook 클래스를 활용하는 LibrarySystem 클래스를 만듭니다.

Use the files provided and the book's code to help.
제공된 파일과 책의 코드를 사용하여 도움을 받으세요.

**파일**

1. `Book.java` (인터페이스)
2. `LibraryBook.java` (Book 구현)
3. `LibrarySystem.java` (LibraryBook 사용)
4. `Main.java` (메인 함수)

## 파일 설명

**`Book.java`**

Create a Book Interface and add the following function definitions.
Book 인터페이스를 만들고 다음 함수 정의를 추가하세요.

```java
String getIsbn();
String getTitle();
String getAuthor();
int getYear();
boolean isAvailable();
void setAvailable(boolean available);
```


**`LibraryBook.java`**

Create a LibraryBook class that implements the Book interface. Add the following instance variables and methods.
Book 인터페이스를 구현하는 LibraryBook 클래스를 만드세요. 다음 인스턴스 변수와 메소드를 추가하세요.

```java
private String isbn;
private String title;
private String author;
private int year;
private boolean available;

public LibraryBook(Book book) {
    // 생성자
}

public LibraryBook(String isbn, String title, String author, int year) {
    // 생성자
}

@Override
public String getIsbn(); // return isbn
public String getTitle(); // return title
public String getAuthor(); // return author
public int getYear(); // return year
public boolean isAvailable(); // return available
public void setAvailable(boolean available);
```

**`LibrarySystem.java`**

Create a LibrarySystem class that contains a list of LibraryBook objects. Add the following instance variables and methods.
LibraryBook 객체 목록을 포함하는 LibrarySystem 클래스를 만드세요. 다음 인스턴스 변수와 메소드를 추가하세요.

Use the 'Java Master' Book Market code to help you.
'Java Master' Book Market 코드를 사용하여 도움을 받으세요.

```java
private Book[] booklist;
private static int bookCount = 0;
private static final int NUM_BOOK = 10;

public LibrarySystem() {
    this.booklist = new Book[NUM_BOOK]; // 생성자
}

public void addBook(Book book) {
    // 책 추가
    // 도움을 위해 Cart.java의 insertBook(Book book)을 참조하세요
}

public void removeBook(String title) {
    // 책 삭제
    // 제공된 코드를 사용하세요
}

public void borrowBook(String title) {
    // 책 대출
    // borrowBook 메소드를 완성하세요
}

public void returnBook(String title) {
    // 책 반납
    // borrowBook 메소드를 참조하여 returnBook 메소드를 직접 작성하세요
}

public void displayBooks() {
    // 책 목록 출력 (책이름, 저자, 출판년도, 대출가능여부 출력)

    /* 
    Expected output:
    "ISBN1234 | JSP 웹 프로그래밍 | 송미영 | 2018 | Available"
    "ISBN1235 | 안드로이드 프로그래밍 | 우재남 | 2022 | Out"
    ...
    */

    // 도움을 위해 Cart.java의 printBookList()를 참조하세요
}
```

**`Main.java`**

Test your code with the provided `Main.java` file.
제공된 `Main.java` 파일로 코드를 테스트하세요.
