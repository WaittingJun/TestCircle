# TestCircle
class Point {
	double x;
	double y;
	Point(double x1, double y1) {
		x = x1;
		y = y1;
	}

	double getX() {return x;}

	double getY() {return y;}

	void setX(double x1) {
		x = x1;
	}

	void setY(double y1) {
		y = y1;
	}	
}

class Circle {

	Point o;
	double r;
	Circle(Point p ,double r1) {
		o = p;
		r = r1;
	}

	Circle(double r1) {
		o = new Point(0.0,0.0);
		r = r1;
	}
	
	double area() {
		return 3.14*r*r;
	}

	Point getO() {return o;}

	double getR() {return r;}

	void setO(double x , double y) {
		o.setX(x);//不太明白
		o.setY(y);
	}
}

public class TestCircle {
	public static void main(String[] args) {
		Circle c1 = new Circle(new Point(1.0,1.0),2.0);
		System.out.println("c1:("+c1.getO().getX()+","+c1.getO().getY()+"),"
					+"r:"+c1.getR());
		
		System.out.println("area="+c1.area());

		c1.setO(5,6);
		System.out.println("c1:("+c1.getO().getX()+","+c1.getO().getY()+"),"
					+"r:"+c1.getR());
	}
}
