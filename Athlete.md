
import java.util.Random;

public abstract class Athlete {
	
	protected static Random rand = new Random(); 
	
	protected String ID;
	protected String name;
	protected int age;
	protected String state;
	
	protected int points;
	
	public Athlete(String _ID, String _name, int _age, String _state) {
		ID = _ID;
		name = _name;
		age = _age;
		state = _state;
		points = 0;
	}

	
	public String getID() {
		return ID;
	}

	public void setID(String iD) {
		ID = iD;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public int getAge() {
		return age;
	}

	public void setAge(int age) {
		this.age = age;
	}

	public String getState() {
		return state;
	}

	public void setState(String state) {
		this.state = state;
	}
	
	
	public void addPoints(int newPts) {
		points += newPts;
	}
	
	public int getPoints() {
		
		return points;
	}
	public abstract int compete();
	
	
	public String toString() {
		
		return String.format("<ID:%s, Name:%s, Age:%d, State:%s, Points:%d>", ID, name, age, state, points);
	}
}
