#ifndef LONG__
#define LONG__

#include <limits.h>

#define LONG_MAX_LENGTH		100

#define LONG_VAR_UINT		
#define LONG_VAR_ULINT	
#define LONG_VAR_ULLINT	


	// adjust program after INT-value, to make program suitable for all systems
#define LONG_CHOSEN_TYPE_VAR	LONG_VAR_ULLINT


#if 	LONG_CHOSEN_TYPE_VAR == LONG_VAR_UINT
#define LONG_VAR_MAX	UINT_MAX
#define INT		unsigned int

#elseif LONG_CHOSEN_TYPE_VAR == LONG_VAR_ULINT
#define LONG_VAR_MAX	ULONG_MAX
#define INT		unsigned long

#elseif LONG_CHOSEN_TYPE_VAR == LONG_VAR_ULLINT
#define LONG_VAR_MAX	ULLONG_MAX
#define INT		unsigned long long int
#endif



#if LONG_VAR_MAX == 	65535			// om sizeof(unsigned int) == 16
#define VAR_HIGH	0xFF00
#define VAR_LOW		0x00FF
#define LONG_PRECISION_PER_INT		2.4082399653118495617099111577959	// =n: 10^n = 2^8

#elseif LONG_VAR_MAX == 4294967295		// om sizeof(unsigned int) == 32
#define VAR_HIGH	0xFFFF0000
#define VAR_LOW		0x0000FFFF
#define LONG_PRECISION_PER_INT		4.8164799306236991234198223155919

#elseif LONG_VAR_MAX == 18446744073709551615 	// if sizeof(unsigned int) == 64
#define VAR_HIGH	0xFFFFFFFF00000000
#define VAR_LOW		0x00000000FFFFFFFF
#define LONG_PRECISION_PER_INT		9.6329598612473982468396446311838
#endif

enum LongRelation {EQUAL, MORE_THAN, MORE_THAN_OR_EQUAL, ...};
enum LongSign {POSITIVE, NEGATIVE, ZERO};
enum LongPrecision {FULL};

	// alltid positivt värde, programmet förutsätter att negativa värden inte uppstår.
	// Long__ kan inte skapas då alla dess konstruktorer och metoder är protected.
class Long__ {
protected;
	INT *x;
	int zero		// x[a] = 0, 0 <= a < zero
	int dec;		// decimal value 	
	int siz;		// total length of Long__
	int prec;		// precision, precisionen är definierad fram till 
		//value of Long_ = sum: x[i] * pow((VAR_LOW+1), dec - i),  zero<=i<siz

	Long__();
	Long__(double f);	// f antas ha så stor precision som är definierat för double:
				// 2^DBL_MANT_DIG ~= 2^53
	Long__(double f, int siz_);	// 
	Long__(double f, int siz_, LongPrecision lp);	// 
	Long__(INT a);		// a kan antas ha en oändlig precision
	Long__(const Long__ A);
	~Long__();

	void addTo(const Long__ A);
	void addTo(INT a);
	Long__ add(INT a);
	Long__ add(const Long__ A);

	void subTo(const Long__ A);
	void subTo(INT a);
	Long__ sub(INT a);
	Long__ sub(const Long__ A);


 	void multiplyTo(const Long__ A);
	void multiplyTo(INT a);	
	Long__ multiply(INT a);
	Long__ multiply(const Long__ A);

	void divideTo(const Long__ A);
	void divideTo(INT A);
	Long__ divide(INT a);
	Long__ divide(const Long__ A);

	bool defined();
	bool define();
	void setPrecision(LongPrecision lp);	// Vid konvergerande iterativa metoder kan 
						// precisionen 
	void 

};

class Long__Test {
public:
	

};


	// kan anta negativa värden, har medlemmen sgn som beskriver dess signum och ärver det positiva reella talet Long__:s egenskaper och värden
class Long_;


class Long_: protected Long__ {
protected:
	LongSign sgn;
};


#endif
