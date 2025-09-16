def get_numeric_input(prompt):
    """A helper function to ensure the user enters a valid number."""
    while True:
        try:
            # Attempt to convert the user's input to a floating-point number
            value = float(input(prompt))
            if value >= 0:
                return value 
            else:
                print("Por favor, digite um número válido.")
        except ValueError:
            # If the conversion fails, inform the user and ask again
            print("Por favor, digite um número válido (ex: 1.99 em vez de 1,99).")

def calculate_interactive_recipe_cost():
    """
    Interactively asks the user for ingredient details to calculate the total recipe cost.
    """
    ingredients_list = []
    total_cost = 0.0

    print("--- 🎂 Calculadora de Custos de Bolo ---")
    print("Adicione cada ingrediente.")
    print("Quando acabar, pressione enter para calcular o total gasto.\n")

    # Main loop to gather information for each ingredient
    while True:
        name = input("Adicione o ingrediente (ou enter para terminar): ").strip()
        
        # If the user enters an empty string, break the loop
        if not name:
            break
        elif not name.isalpha():
            print("Por favor, digite um ingrediente válido.")
            name = input("Adicione o ingrediente (ou enter para terminar): ").strip()
        # --- Gather Ingredient Details from User ---
        print(f"\n--- Detalhes para {name.capitalize()} ---")
        recipe_qty = get_numeric_input(f"Quantidade usada de '{name}': ")
        unit = input(f"Unidade para '{name}' (ex: g, ml, un): ").strip()
        store_qty = get_numeric_input("Tamanho do pacote? (ex: 10 para uma caixa de ovos, 1000 para um pacote de 1kg): ")
        store_price = get_numeric_input(f"Qual o preço de compra de {store_qty} {unit}?: €")

        # --- Perform Calculation ---
        # The formula remains: (amount_needed / amount_in_package) * price_of_package
        ingredient_cost = (recipe_qty / store_qty) * store_price
        total_cost += ingredient_cost

        # Store the results for the final summary
        ingredients_list.append({
            'name': name,
           'cost': ingredient_cost,
            'quantity': recipe_qty,
            'unit': unit
        })
        
        print(f"✅ Custo para {name.capitalize()} adicionado: €{ingredient_cost:.2f}\n")

    # --- Print Final Summary ---
    if ingredients_list:
        print("\n--- ✅ Preço Final ---")
        for item in ingredients_list:
            # Create a formatted string for the description part
            description = f"{item['name'].capitalize()} ({item['quantity']} {item['unit']})"
            print(f"{description:<28}: €{item['cost']:.2f}")
        
        print("--------------------------------------")
        print(f"{'Preço Total da Receita':<20}: €{total_cost:.2f}")
        print("--------------------------------------")
    else:
        print("\nNenhum ingrediente adicionado. Nenhum valor foi calculado.")

# Run the main function when the script is executed
if __name__ == "__main__":
    calculate_interactive_recipe_cost()
