Genrator-NumberCard-Name-Adress
===============================
 

public class GeneratorNom {
	static int c;
	static String[] Nom_Aleatoire = { "FREDDY", "JOHN", "JAC", "PAUL",
			"LAFOUINE", "TINTIN", "TITO" };
	static String[] PostNom_Aleatoire = { "MAKIADI", "DESJARDIN", "PAPIN",
			"BERRI" };
	static String[] Adresse = { "MATETE", "LEMBA", "KINGASANI", "NDJILI",
			"NGALIEMA" };
	public static String[] CARD_PREFIX_LIST = { "5039", "5056", "5016", "5032",
			"5029", "4024", "5085", "5016"};

	public static void main(String[] args) {
		String DevNom = NomAleatoire();
		String DevPostNom = PostNom();
		String DevAdress = Adresse();
		int gen44 = NumeroMaison();
		// generateur nom
				double gen1 = Math.random() * 7;
				int gen11 = (int) gen1;
				String CARD_Exemple = CARD_PREFIX_LIST[gen11];
		System.out.println("Nom :     " + DevNom + "  " + DevPostNom + "\n"
				+ "Adresse : " + DevAdress + " No " + gen44);
		
		// generateur carte bancaire
		System.out.print("CARTE BANCAIRE : ");
		System.out.print(CARD_Exemple);
		System.out.print(" ");
		int Co = 0;
		do {
			c = 0;
			do {
				double gen5 = Math.random() * 10;
				int gen55 = (int) gen5;
				System.out.print(gen55);
				c++;
			} while (c != 4);
			System.out.print(" ");
			Co++;
		} while (Co != 3);

	}

	private static int NumeroMaison() {
		// generateur numero
		double gen4 = Math.random() * 100;
		int gen44 = (int) gen4 + 1;
		return gen44;
	}

	private static String Adresse() {
		// generateur adresse
		double gen3 = Math.random() * 5;
		int gen33 = (int) gen3;
		String DevAdress = Adresse[gen33];
		return DevAdress;
	}

	private static String PostNom() {
		// generateur postnom
		double gen2 = Math.random() * 4;
		int gen22 = (int) gen2;
		String DevPostNom = PostNom_Aleatoire[gen22];
		return DevPostNom;
	}

	private static String NomAleatoire() {
		// generateur nom
		double gen1 = Math.random() * 7;
		int gen11 = (int) gen1;
		String DevNom = Nom_Aleatoire[gen11];
		return DevNom;
	}

}

