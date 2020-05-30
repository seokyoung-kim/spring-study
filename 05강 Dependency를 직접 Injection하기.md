## Dependncy 직접 Injection하기
```
public class Program {
	public static void main(String[] args) {
		Exam exam = new NewlecExam();
		ExamConsole console = new InlineExamConsole(exam);
		console.print();
	}
}
```
ExamConsole console = 뒤에 오는 생성자를 변경함으로써 부품을 갈아끼우듯 Dependency를 직접 Injection함.