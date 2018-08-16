#include <iostream>
#include <math.h>

using namespace std;

#define alpha 1.24

extern unsigned int var;

void calcParabolico(void);
void print_results(void);


int main()
{
    unsigned short int tresdes = 5;
    //lib_func1();
    int var = 100;

    var += tresdes;

    //Calculando los parametros en la Tierra con g = 9.8 m/s*s
    calcParabolico();
    print_results();

    //Calculando los parametros en la Luna con g = 1.62 m/s*s
    calcParabolico();
    print_results();


    return 0;
}

void calcParabolico(void)
{
    const float g = 9.8;
    extern double vx0, vy0, x, y, vx, vy, v0, y0, t;
//v0=0;
//t=0;
    vx0 = v0 * cos(alpha);
    vy0 = v0 * sin(alpha);

    vx = vx0;
    vy = vy0-g*t;

    x = vx*t;
    y = y0+vy0*t-(g*pow(t,2)/2);
}

void print_results(void)
{
    extern double vx0, vy0, x, y, vx, vy, v0, y0, t;
    std::cout<<"Los resultados del calculo parabolico son: "<<std::endl;
    std::cout<<"Velocidad en x: "<<vx<<", ";
    std::cout<<"Velocidad en y: "<<vy<<", ";
    std::cout<<"Posicion en x: "<<x<<", ";
    std::cout<<"Posicion en y: "<<y<<std::endl;
}

void otros_calculos(void)
{
    double var1=0;
    /* Serie simple (1/[(x^2) + (x+1)]) para x entre 1 y 199*/
    for(int x=1; x<200; x++)
    
      var=(1/((x^2) + (x + 1)));
      
        /* Volumen de la esfera */
      //Agregue aqui la formula
      
      double volumen=0; 
      float pi = 3.14;
      volumen= 4/3 * pi * (x^3);
       

 
double Raices=0;
    /* Raices de la ecuacion (3*x^2) + (5*x) + 8  = 0 */
     Raices = (3* (x^2)) + (5*x) + 8  = 0

double Z0, w, mu, epsi, betacero;

int R, L, G, C, f, B, a, b;
f = 10
w=2* pi* f
    /* Impedancia tipica de una linea de transmision
     * Z0 = [(R+wL)/(G+wC)]^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 10kHz */
        //Agregue aqui la formula
Z0 = ((R+wL)/(G+wC)) ^ (1/2)

    /* Constante de fase de una fibra optica
    
    
     * B = {[((a^2)-(b^2))*c+(b^2)]^(1/2)}*betacero
     * betacero = w*(mu*epsi)^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 5GHz
     * mu = 0.00000125664
     * epsi = 0.00000000000088542  */

mu = 0.00000125664
epsi = 0.00000000000088542
betacero = w*(mu*epsi)^(1/2)
B = ((a^2)-(b^2))*c+(b^2)^(1/2)*betacero
}
