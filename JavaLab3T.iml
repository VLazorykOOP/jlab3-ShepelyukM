package laba3;

public class Engine {
    private double power; // потужність двигуна в кіловатах
    private double torque; // крутний момент двигуна в ньютон-метрах

    public Engine(double power, double torque) {
        this.power = power;
        this.torque = torque;
    }

    public void show() {
        System.out.println("Engine power: " + power + " kW");
        System.out.println("Engine torque: " + torque + " Nm");
    }
}
class DieselEngine extends InternalCombustionEngine {
    private boolean hasTurbocharger; // наявність турбонадуву

    public DieselEngine(double power, double torque, int cylinders, boolean hasTurbocharger) {
        super(power, torque, cylinders, "Diesel");
        this.hasTurbocharger = hasTurbocharger;
    }

    public void show() {
        super.show();
        System.out.println("Has turbocharger: " + hasTurbocharger);
    }
}
class InternalCombustionEngine extends Engine {
    private int cylinders; // кількість циліндрів
    private String fuelType; // тип палива (бензин, дизель, газ)

    public InternalCombustionEngine(double power, double torque, int cylinders, String fuelType) {
        super(power, torque);
        this.cylinders = cylinders;
        this.fuelType = fuelType;
    }

    public void show() {
        super.show();
        System.out.println("Number of cylinders: " + cylinders);
        System.out.println("Fuel type: " + fuelType);
    }
}
class JetEngine extends Engine {
    private double thrust; // тяга двигуна в кілограмах-сили

    public JetEngine(double power, double thrust) {
        super(power, 0); // тяга реактивного двигуна визначається окремо
        this.thrust = thrust;
    }

    public void show() {
        super.show();
        System.out.println("Thrust: " + thrust + " kgf");
    }
}
public class EngineMain {
    public static void main(String[] args) {
        Engine[] engines = new Engine[4];
        engines[0] = new Engine(100, 200);
        engines[1] = new InternalCombustionEngine(150, 300, 4, "Gasoline");
        engines[2] = new DieselEngine(200, 400, 6, true);
        engines[3] = new JetEngine(5000, 10000);

        for (Engine engine : engines) {
            engine.show();
            System.out.println();
        }
    }
}
----------------------------------------------------
package laba33;

interface INorm {
    double calculateNorm();
}
package laba33;

class Vector2D implements INorm {
    private double x;
    private double y;

    public Vector2D(double x, double y) {
        this.x = x;
        this.y = y;
    }

    public double getX() {
        return x;
    }

    public void setX(double x) {
        this.x = x;
    }

    public double getY() {
        return y;
    }

    public void setY(double y) {
        this.y = y;
    }

    public double calculateNorm() {
        return Math.sqrt(x * x + y * y);
    }

    @Override
    public String toString() {
        return "Vector2D{" +
                "x=" + x +
                ", y=" + y +
                '}';
    }

    @Override
    public boolean equals(Object o) {
        if (this == o)
            return true;
        if (o == null || getClass() != o.getClass())
            return false;
        Vector2D vector2D = (Vector2D) o;
        return Double.compare(vector2D.x, x) == 0 &&
                Double.compare(vector2D.y, y) == 0;
    }
}
class Vector3D implements INorm {
    private double x;
    private double y;
    private double z;

    public Vector3D(double x, double y, double z) {
        this.x = x;
        this.y = y;
        this.z = z;
    }

    public double getX() {
        return x;
    }

    public void setX(double x) {
        this.x = x;
    }

    public double getY() {
        return y;
    }

    public void setY(double y) {
        this.y = y;
    }

    public double getZ() {
        return z;
    }

    public void setZ(double z) {
        this.z = z;
    }

    public double calculateNorm() {
        return Math.sqrt(x * x + y * y + z * z);
    }

    @Override
    public String toString() {
        return "Vector3D{" +
                "x=" + x +
                ", y=" + y +
                ", z=" + z +
                '}';
    }

    @Override
    public boolean equals(Object o) {
        if (this == o)
            return true;
        if (o == null || getClass() != o.getClass())
            return false;
        Vector3D vector3D = (Vector3D) o;
        return Double.compare(vector3D.x, x) == 0 &&
                Double.compare(vector3D.y, y) == 0 &&
                Double.compare(vector3D.z, z) == 0;
    }
}
public class INormMain {
    public static void main(String[] args) {
        INorm[] vectors = new INorm[3];

        Vector2D v1 = new Vector2D(3, 4);
        Vector3D v2 = new Vector3D(1, 2, 3);
        Vector2D v3 = new Vector2D(-2, 5);

        vectors[0] = v1;
        vectors[1] = v2;
        vectors[2] = v3;

        for (INorm vector : vectors) {
            System.out.println(vector.toString());
            System.out.println("Norm: " + vector.calculateNorm());
            System.out.println();
        }
    }
}
