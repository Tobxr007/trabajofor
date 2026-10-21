#include <iostream>
#include <cmath>
using namespace std;

// Funcion para calcular el area de un cuadrado
float areaCuadrado(float lado) {
    return lado * lado;
}

// Funcion para calcular el volumen de un cilindro
float volumenCilindro(float radio, float altura) {
    return 3.1416 * radio * radio * altura;
}

// Funcion para calcular el volumen de una esfera
float volumenEsfera(float radio) {
    return (4.0 / 3.0) * 3.1416 * pow(radio, 3);
}

int main() {
    int opcion;
    float lado, radio, altura, resultado;

    do {
        cout << "\n--- MENU DE FIGURAS GEOMETRICAS ---" << endl;
        cout << "1. Area de un cuadrado" << endl;
        cout << "2. Volumen de un cilindro" << endl;
        cout << "3. Volumen de una esfera" << endl;
        cout << "4. Salir" << endl;
        cout << "Seleccione una opcion: ";
        cin >> opcion;

        switch (opcion) {
            case 1:
                cout << "Ingrese el lado del cuadrado: ";
                cin >> lado;

                if (lado > 0) {
                    resultado = areaCuadrado(lado);
                    cout << "Area del cuadrado: "
                         << resultado << endl;
                } else {
                    cout << "El lado debe ser mayor que cero." << endl;
                }
                break;

            case 2:
                cout << "Ingrese el radio del cilindro: ";
                cin >> radio;
                cout << "Ingrese la altura del cilindro: ";
                cin >> altura;

                if (radio > 0 && altura > 0) {
                    resultado = volumenCilindro(radio, altura);
                    cout << "Volumen del cilindro: "
                         << resultado << endl;
                } else {
                    cout << "Los valores deben ser mayores que cero." << endl;
                }
                break;

            case 3:
                cout << "Ingrese el radio de la esfera: ";
                cin >> radio;

                if (radio > 0) {
                    resultado = volumenEsfera(radio);
                    cout << "Volumen de la esfera: "
                         << resultado << endl;
                } else {
                    cout << "El radio debe ser mayor que cero." << endl;
                }
                break;

            case 4:
                cout << "Saliendo del programa..." << endl;
                break;

            default:
                cout << "Opcion no valida. Intente de nuevo." << endl;
        }

    } while (opcion != 4);

    return 0;
}
