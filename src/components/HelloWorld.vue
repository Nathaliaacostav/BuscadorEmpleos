<template>
    <div class="job-card">
        <div class="job-image">
            <img src="https://res.cloudinary.com/dhhyc88td/image/upload/v1709063912/company_2_tlbqn8.svg" alt="Imagen de empresa">
        </div>
        <div class="job-details">
            <div class="job-title">
                <h2>Cargo del empleo</h2>
                <div class="skills">
                    <span>Habilidades requeridas:</span>
                    <ul>
                        <li>JavaScript</li>
                        <li>React</li>
                        <li>Node.js</li>
                    </ul>
                </div>
            </div>
            <div class="company-info">
                <p>Nombre de la empresa: TechSolutions S.A.S.</p>
                <p>Modalidad de trabajo: Remoto</p>
                <p>Salario: $4,000,000 - $6,000,000</p>
                <p>Vacantes: 2</p>
            </div>
            <div class="additional-info">
                <p>Hora de publicación: 2024-02-26T09:00:00Z</p>
                <div class="icons">
                    <!-- Aquí coloca los íconos -->
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {

}
</script>


<style scoped>
.job-card {
    display: flex;
    background-color: #ffffff;
    border: 1px solid #dddddd;
    border-radius: 5px;
    margin-bottom: 20px;
    transition: box-shadow 0.3s ease;
}

.job-card:hover {
    box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.2);
}

.job-image {
    width: 30%;
}

.job-image img {
    width: 100%;
    height: auto;
}

.job-details {
    width: 70%;
    padding: 20px;
}

.job-title h2 {
    color: #000000;
    margin-bottom: 10px;
}

.skills {
    color: #333333;
}

.company-info p {
    color: #333333;
    margin-bottom: 5px;
}

.additional-info p {
    color: #333333;
    margin-bottom: 5px;
}

.icons {
    /* Estilos para los íconos */
}
</style>