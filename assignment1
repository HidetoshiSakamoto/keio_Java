package myproj;
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solve_repeatedly_quadratic_equation {

	public static void main(String[] args) {
		// TODO 自動生成されたメソッド・スタブ
		System.out.println("quitと入力されるまで2次方程式を繰り返し解きます");
		System.out.println("a,b,cの形で入力してください");
		InputStreamReader isr = new InputStreamReader(System.in);
		BufferedReader reader = new BufferedReader(isr);

		while(true) {
			try {
				String line = reader.readLine();
				String ans;
				if (line.equals("quit")) {
					System.out.println("終了します");
					break;
				}else{
					String lst[] = line.split(",");
					double a = Double.parseDouble(lst[0]);
					double b = Double.parseDouble(lst[1]);
					double c = Double.parseDouble(lst[2]);

					if(a==0) {
						ans = "aが0なため答えは"+String.valueOf(-c/b)+"です";
					}else {
						ans = solve(a,b,c);
					}
				}
				System.out.println(ans);
				System.out.println("もう一度二次方程式を解くならa,b,cの形で入力を、終了する場合はquitを入力してください");
			} catch(IOException e) {
				System.out.println(e);
			}
		}
	}
	public static String solve(double a,double b,double c) {
		Double judge = Math.pow(b, 2) - 4 * a * c;
		String ans;
		if(judge < 0){
			ans = "判別式が負なため、この二次方程式には実数解が存在しません";
		} else {
			double ans_alpha = ((-b + Math.sqrt(judge)) / (2 * a));
			double ans_beta = ((-b - Math.sqrt(judge)) / (2 * a));
			ans = "二次方程式の解は"+String.valueOf(ans_alpha)+"と"+String.valueOf(ans_beta)+"です";
		}
		return ans;
	}
}
