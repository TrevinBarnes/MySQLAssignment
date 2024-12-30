DROP TABLE IF EXISTS projects;
DROP TABLE IF EXISTS material;
DROP TABLE IF EXISTS step;
DROP TABLE IF EXISTS category;
DROP TABLE IF EXISTS projects_category;

CREATE TABLE projects_category (
	projects_id INT NOT NULL,
	category_id INT NOT NULL,
	FOREIGN KEY(projects_id) REFRENCES projects (projects_id) ON DELETE CASCACDE,
	FOREIGN KEY (category_id) REFRENCES category (category_id) ON DELETE CASCADE,
	UNIQUE KEY (projects_id,category_id)
);

CREATE TABLE category (
	category_id INT NOT NULL,
	category_name VARCHAR(128) NOT NULL,
	PRIMARY KEY (category_id)
);


CREATE TABLE step (
	step_id INT /*AUTO_INCREMENT*/ NOT NULL,
	projects_id INT NOT NULL,
	step_order INT NOT NULL,
	step_text TEXT NOT NULL,
	PRIMARY KEY(step_id),
	FOREIGN KEY(projects_id) REFRENCES projects (projects_id) ON DELETE CASCACDE,
);


CREATE TABLE material (
	material_id INT /*AUTO_INCREMENT*/ NOT NULL,
	projects_id INT NOT NULL,
	material_name VARCHAR(128) NOT NULL,
	num_required INT,
	cost DECIMAL(7,2),
	PRIMARY KEY(material_id),
	FOREIGN KEY(projects_id) REFRENCES projects (projects_id) ON DELETE CASCACDE,
);


CREATE TABLE projects (
	projects_id INT /*AUTO_INCREMENT*/ NOT NULL,
	projects_name VARCHAR (128) NOT NULL,
	estimated_hours DECIMAL(7,2),
	actual_hours DECIMAL(7,2),
	difficulty INT,
	notes TEXT,
	PRIMARY KEY (projects_id)
);